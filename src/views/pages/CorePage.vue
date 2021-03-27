<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-12 col-md-5">
        <inputs :info="info" />
      </div>
      <div class="col-12 col-md-5">
        <detail :info="info" />
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

<style scoped></style>
