<script>
      import StatusBox from './StatusBox.vue';
      export default {
            components: {
            StatusBox
            }
      }
</script>

<template>
      <div class="calendar-grid">
            <div class="calendar-header">
                  <div class="filler shift-left">
                        <button>
                              <img src="../assets/icons/Pil-ned.svg" alt="">
                        </button>
                  </div>
                  <div class="dates">
                         <div class="date-cell" v-for="n in 20" :key="'date-' + n">{{ n }}</div>
                  </div>
                  <div class="filler">
                        <button>
                              <img src="../assets/icons/Pil-ned.svg" alt="">
                        </button>
                  </div>
                  
                  
            </div>
            <div class="calendar-view">
                  <div class="employee-row">
                        <div class="employee-name">
                              Jane Doe
                        </div>
                        <div class="statuses">
                              <StatusBox status="available" />
                              <StatusBox status="available" />
                              <StatusBox status="half-booked" />
                              <StatusBox status="full-booked" />
                              <StatusBox status="available" />
                              <StatusBox status="absent" />
                              <StatusBox status="available" />
                              <StatusBox status="prel-half" />
                              <StatusBox status="prel-full" />
                              <StatusBox status="available" />
                              <StatusBox status="available" />
                              <StatusBox status="half-booked" />
                              <StatusBox status="full-booked" />
                              <StatusBox status="available" />
                              <StatusBox status="absent" />
                              <StatusBox status="available" />
                              <StatusBox status="prel-half" />
                              <StatusBox status="prel-full" />
                              <StatusBox status="absent" />
                              <StatusBox status="available" />
                        </div>
                        <div class="filler">

                        </div>
                  </div>
                  
                  <div class="employee-row">
                        <div class="employee-name">
                              Super Mario
                        </div>
                        <div class="statuses">
                              <StatusBox status="available" />
                              <StatusBox status="half-booked" />
                              <StatusBox status="full-booked" />
                              <StatusBox status="absent" />
                              <StatusBox status="available" />
                              <StatusBox status="prel-half" />
                              <StatusBox status="prel-full" />
                              <StatusBox status="available" />
                              <StatusBox status="available" />
                              <StatusBox status="half-booked" />
                              <StatusBox status="absent" />
                              <StatusBox status="full-booked" />
                              <StatusBox status="available" />
                              <StatusBox status="available" />
                              <StatusBox status="prel-full" />
                              <StatusBox status="prel-half" />
                              <StatusBox status="absent" />
                              <StatusBox status="available" />
                              <StatusBox status="available" />
                              <StatusBox status="available" />
                        </div>
                        <div class="filler">

                        </div>
                  </div>
                  
            </div>
            
           
      </div>
</template>

<style scoped>

      button {           
            border: 0;
            background-color: white;
            cursor: pointer;
      }

      
      
      
      .calendar {
            display: grid;
            grid-template-columns: 2fr repeat(20, 1fr) .5fr;
      }
      
      .nav {
            grid-column: span 22;
      }
      
      .calendar-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 0.5rem;
      }
      
      .dates {
            display: grid;
            grid-template-columns: repeat(20, 1fr);
            gap: 0.25rem;
            flex: 1;
            
      }
      
      .date-cell {
            display: flex;
            align-items: center;    /* Vertical centering */
            justify-content: center; /* Horizontal centering */
            height: 2rem;
            width: 2rem;
            justify-self: center;         /* Or whatever height you want */
            padding: auto;
            background-color: #EDEDED;
            border-radius: 50%;
      }
      
      .employee-row {
            display: flex;
            align-items: center;
            gap: 1rem;
            
      }
      
      .employee-name {
            min-width: 5rem;
            max-width: 5rem;
      }
      
      .statuses {
            display: grid;
            grid-template-columns: repeat(20, 1fr);
            gap: 0.25rem;
            flex: 1;
            justify-items: center;
            padding: .3rem 0 ;
            box-sizing: border-box;
            background-color: #EDEDED;
      }
      .filler {
            min-width: 5rem;
            background-color: white;
      }

      .shift-left{
            display: flex;
            justify-content: flex-end;
      }
      .calendar-view {
            display: flex;
            flex-direction: column;
            gap: .5rem;
      }
</style>