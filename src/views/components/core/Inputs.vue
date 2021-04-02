<template>
  <div class="card">
    <div class="card-body">
      <div class="card-title"><h5>Вводные Данные</h5></div>
      <form>
        <div class="mb-3">
          <input
            type="text"
            class="form-control"
            placeholder="name"
            v-model="info.name"
          />
        </div>
        <div class="mb-3">
          <input
            type="text"
            class="form-control"
            placeholder="surname"
            v-model="info.surname"
          />
        </div>
        <div class="mb-3">
          <datepicker
            :bootstrap-styling="true"
            placeholder="Select Date"
            v-model="info.birthDate"
          ></datepicker>
        </div>
        <div class="mb-3">
          <select class="form-select" v-model="info.select">
            <option value="" selected disabled>(select)</option>
            <option value="Star">Star</option>
            <option value="Heart">Heart</option>
            <option value="Octagon">Octagon</option>
          </select>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import Datepicker from "vuejs-datepicker";
export default {
  name: "Inputs",
  props: {
    info: Object,
  },
  components: {
    Datepicker,
  },
};
</script>

<style scoped>
.card {
  padding: 5px;
  height: 280px;
  background-color: azure;
}
</style>
