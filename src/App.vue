<script setup>
import SelectBox from './components/SelectBox.vue';

</script>

<template>

  <header>
    <nav>
      <div class="filter-container">
        <label>Filter
          <img src="/src/assets/icons/Vector.svg">
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
      <img src="/src/assets/icons/Vector.svg">
    </label>

    <div class="profession-container">
      <Profession img_src="/src/assets/icons/arcticons_hammer.svg" alt="Blabla" label="Snickare"/>

    </div>
  </div>

</template>

<script>
import Profession from './components/Profession.vue'
import SelectBox from './components/SelectBox.vue'
export default {
  name: 'App',
  components: {
    SelectBox
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
  display:flex;
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
</style>
