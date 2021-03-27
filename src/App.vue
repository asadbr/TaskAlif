<template>
  <div id="app">
    <CorePage />
  </div>
</template>
<script>
export default {
  components: { CorePage: () => import("@/views/pages/CorePage") },
};
</script>
