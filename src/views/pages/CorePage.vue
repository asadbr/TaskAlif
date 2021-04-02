<template>
  <div class="body min-vh-100 d-flex justify-content-center align-items-center">
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-4">
          <inputs :info="info" />
        </div>
        <div class="col-12 col-md-3">
          <detail :info="info" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Inputs from "@/views/components/core/Inputs";
import Detail from "@/views/components/core/Detail";
export default {
  name: "CorePage",
  components: { Detail, Inputs },
  data() {
    return {
      info: {
        name: "",
        surname: "",
        birthDate: "",
        select: "",
      },
    };
  },
  watch: {
    info: {
      handler() {
        if (Object.values(this.info).every((item) => item.length !== 0)) {
          console.log(JSON.stringify(this.info));
        }
      },
      deep: true,
    },
  },
};
</script>

<style scoped>
.row {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.body {
  background-color: slategray;
}
</style>
