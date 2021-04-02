<template>
  <div class="card shadow-sm">
    <div class="card-body d-flex flex-column justify-content-start">
      <div class="class-title"><h5>Информации</h5></div>
      <p class="name mt-3">Name: {{ info.name }}</p>
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
  height: 280px;
}
</style>
