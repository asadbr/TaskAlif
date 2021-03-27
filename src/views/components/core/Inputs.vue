<template>
  <div class="card">
    <div class="card-body">
      <div class="card-title"><h5>Вводные Данные</h5></div>
      <form>
        <div class="mb-3">
          <input
            type="text"
            class="form-control"
            aria-describedby="emailHelp"
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
          <input
            type="date"
            class="form-control"
            placeholder="birth date"
            v-model="info.birthDate"
          />
        </div>
        <div class="mb-3">
          <select
            class="form-select"
            aria-label="Default select example"
            v-model="info.select"
          >
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
export default {
  name: "Inputs",
  props: {
    info: Object,
  },
};
</script>

<style scoped></style>
