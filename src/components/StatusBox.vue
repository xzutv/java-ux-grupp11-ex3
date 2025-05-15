<script>
      export default {
            props: {
                  status: {
                        type: String, 
                        required: true
                  }
            },
            computed: {
                  oddClass() {
                        return `odd-${this.status}`;
                  },
                  evenClass() {
                        return `even-${this.status}`;
                  }
            }
      }
</script>

<style scoped>
      .status-box {
            min-width: 1rem;
            min-width: 1rem;
            margin: 0 .5;
      }

      .status-box div {
            height: .3rem;
            width: 2rem;
      }

      .odd-available, .even-available {
            background-color: #BAD19E;
      }

      .odd-full-booked, .even-full-booked {
            background-color: #D59ECF;
      }

      .odd-half-booked, .even-half-booked {
            background-color: #3A5D7A;
      }

      .odd-absent, .even-absent {
            background-color: #404040;
      }

      /* preliminary booked 100%, we only set odd divs to a color */
      .odd-prel-full {
            background-color: #D59ECF;
      }

       /* preliminary booked 50%, we only set odd divs to a color  */
      .odd-prel-half {
            background-color: #3A5D7A;
      }
      .even-prel-half {
            background-color: #404040;
      }




</style>

<template>
      <div class="status-box">
            <div :class="oddClass"></div>
            <div :class="evenClass"></div>
            <div :class="oddClass"></div>
            <div :class="evenClass"></div>
            <div :class="oddClass"></div>
            <div :class="evenClass"></div>
      </div>
</template>