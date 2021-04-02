<template>
  <div class="card">
    <div class="card-body">
      <div class="class-title"><h5>Информации</h5></div>
      <p>Name: {{ info.name }}</p>
      <p>Surname: {{ info.surname }}</p>
      <p>
        Birth-Date:
        <span v-if="info.birthDate">
          {{ new Date(info.birthDate).getDate() }}/{{
            new Date(info.birthDate).getMonth()
          }}/{{ new Date(info.birthDate).getFullYear() }}
        </span>
      </p>
      <p>(select): {{ info.select }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Detail",
  props: {
    info: Object,
  },
};
</script>

<style scoped>
.card {
  background-color: azure;
}
</style>
