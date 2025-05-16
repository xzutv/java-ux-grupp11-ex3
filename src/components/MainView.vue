<script>
import StatusBox from './StatusBox.vue';
import ProfileCard from './ProfileCard.vue';

export default {
      components: {
            StatusBox, ProfileCard
      }
}
</script>

<template>
      <div class="calendar">
            <div class="calendar-header">
                  <div class="filler shift-left">
                        <button>
                              <img src="../assets/icons/Pil-ned.svg" alt="">
                        </button>
                  </div>
                  <div class="dates">
                        <div class="date-cell" v-for="n in 20" :key="'date-' + n">{{ n }}</div>
                  </div>
                  <div class="shift-right">
      
                        <img src="../assets/icons/Pil-ned.svg" alt="">
      
                  </div>
            </div>
            <div class="calendar-view">
                  <div class="employee-row">
                        <ProfileCard name="Jane Doe" src="/src/assets/icons/Ellipse 5.svg" alt="Person"></ProfileCard>
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
      
}

.nav {
      grid-column: span 22;
}

.calendar-header {
      
      display: grid;
      grid-template-columns: 6rem 1fr 0rem; /* left / center / right */
      align-items: center;
      margin-bottom: 0.5rem;
      

}

.dates {
      display: grid;
      grid-template-columns: repeat(20, 1fr);
      
      flex: 1;

}

.date-cell {
      display: flex;
      align-items: center;
      /* Vertical centering */
      justify-content: center;
      /* Horizontal centering */
      height: 2rem;
      width: 2rem;
      justify-self: center;
      /* Or whatever height you want */
      padding: auto;
      background-color: #EDEDED;
      border-radius: 50%;
}

.employee-row {
      display: flex;
      align-items: center;
      gap: 1rem;
      padding: .3rem 0;
      max-height: 2rem;
      background-color: #EDEDED;
      min-width: 300px

}

.employee-name {
      min-width: 5rem;
      max-width: 5rem;
}

.statuses {
      display: grid;
      grid-template-columns: repeat(20, 1fr);
     
      flex: 1;
      justify-items: center;
}

.filler {
      min-width: 5rem;
}

.shift-left {
      display: flex;
      justify-content: flex-end;
}

.shift-right {
      
}

.calendar-view {
      display: flex;
      flex-direction: column;
      gap: .5rem;
}
</style>