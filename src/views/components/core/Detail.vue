<template>
  <div class="card">
    <div class="card-body">
      <div class="class-title"><h5>Информации</h5></div>
      <p>Name: {{ info.name }}</p>
      <p>Surname: {{ info.surname }}</p>
      <p>Birth-Date: {{ info.birthDate }}</p>
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

<style scoped></style>
