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
            position: relative;
            height: auto;
            width: auto;
            display: flex;
            flex-direction: column;
            align-items: center;
      }

      .status-box div {
            height: 0.3rem;
            width: 3rem;
      }

      .status-label {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 0.75rem;
            pointer-events: none;
            z-index: 1;
            color: white;
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
            <span class="status-label">{{ status }}</span>

            <div :class="oddClass"></div>
            <div :class="evenClass"></div>
            <div :class="oddClass"></div>
            <div :class="evenClass"></div>
            <div :class="oddClass"></div>
            <div :class="evenClass"></div>
            <div :class="oddClass"></div>
      </div>
</template>