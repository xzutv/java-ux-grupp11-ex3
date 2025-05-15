<script setup>
import Profession from './components/Profession.vue'
import SelectBox from './components/SelectBox.vue';
import StatusBox from './components/StatusBox.vue';
import MainView from './components/MainView.vue';
import ProfileCard from './components/ProfileCard.vue';
</script>

<template>

  <header>
    <nav>
      <div class="filter-container">
        <label>Filter
          <img src="/src/assets/icons/Pil-ned.svg">
        </label>
        <div class="box-container">
          <SelectBox label="Personer" :options="people" v-model="selectedPerson" />
          <SelectBox label="Yrkesroll" :options="roles" v-model="selectedRole" />
          <SelectBox label="Bokningstyp" :options="bookingTypes" v-model="selectedBookingType" />
        </div>
      </div>
    </nav>
  </header>

  <div class="work-plan-container">
    <label>Planera arbete
      <img src="/src/assets/icons/Pil-ned.svg">
    </label>

    <div class="profession-container">
      <Profession img_src="/src/assets/icons/hammer.svg" alt="Hammare ikon" label="Snickare" />
      <Profession img_src="/src/assets/icons/roller.svg" alt="Pensel ikon" label="Målare" />
      <Profession img_src="/src/assets/icons/electricity.svg" alt="Lamp ikon" label="Elektriker" />
      <Profession img_src="/src/assets/icons/pipe.svg" alt="Rör ikon" label="Rörmokare" />
      <Profession img_src="/src/assets/icons/bricks.svg" alt="Mur ikon" label="Murare" />

    </div>

    <!-- <div class="book-button"> -->
    <button class="book-button">Boka</button>
  </div>
  <!-- </div> -->

  <div class="status-legend">
    <div class="legend-item">
      <StatusBox status="available" />
      Tillgänglig
    </div>
    <div class="legend-item">
      <StatusBox status="full-booked" />
      Fullbokad
    </div>
    <div class="legend-item">
      <StatusBox status="half-booked" />
      Bokad 50%
    </div>
    <div class="legend-item">
      <StatusBox status="prel-full" />
      Preliminärt fullbokad
    </div>
    <div class="legend-item">
      <StatusBox status="prel-half" />
      Preliminärt bokad 50%
    </div>
    <div class="legend-item">
      <StatusBox status="absent" />
      Frånvaro
    </div>
  </div>

  <div>
    <MainView></MainView>
  </div>
</template>






<script>

export default {
  name: 'App',
  components: {
    SelectBox, StatusBox, SelectBox, Profession, ProfileCard
  },
  data() {
    return {
      people: [
        { id: 'p1', name: 'Göran Atlas' },
        { id: 'p2', name: 'Annik Rufus' },
      ],
      roles: [
        { id: 'r1', name: 'Elektriker' },
        { id: 'r2', name: 'Snickare' },
        { id: 'r3', name: 'Rörläggare' },
        { id: 'r4', name: 'Målare' }
      ],
      bookingTypes: [
        { id: 'b1', name: '100%' },
        { id: 'b2', name: '50%' }
      ],

    }
  },
  methods: {

  }
}
</script>


<style scoped>
header {

  /* color: gray; */

}

nav {
  display: flex;
  padding: 1.25rem;
  background-color: #EDEDED;
  margin-bottom: 10px;

}

.box-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 2.5rem;
  max-width: 3rem;
}

.status-legend {
  display: flex;
  gap: 2rem;
  justify-self: center;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: .5rem;
}


.work-plan-container {
  background-color: #EDEDED;
  padding: 20px 20px;
  gap: 40px;
  border-radius: 10px;
  gap: 13px;

}

.profession-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 10px;
}

.book-button {
  display: flex;
  justify-self: flex-end;
  border: none;
  width: 200px;
  padding: 10px;
  margin-right: 10px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 10px;
  background: #FFF;
  cursor: pointer;
}

</style>
