<template>
  <div class="home">
    <div class="dashboard">
      <Asider />
      <Main-content />
    </div>
  </div>
</template>

<script>
import Asider from '../components/Asider.vue';
import MainContent from '../components/MainContent.vue';
export default {
  components: { Asider, MainContent },
  name: "Home",
  
};
</script>

<style lang="scss">
.dashboard {
  display: grid;
  grid-template-columns: 20% 80%
}
</style>