<script>
import appHeader from './components/appHeader.vue';

export default {
  components: {
    appHeader,
  },
};
</script>

<template>
  <appHeader />
  <main>
    <div class="backgroundbox">
      <!-- Contenuto del box qui -->
    </div>
  </main>
</template>

<style lang="scss">
@use './styles/partials/_variables' as *;
@use './styles/_general.scss' as *;

.backgroundbox {
  height: 300px;
  background-image: url('public/jumbotron.jpg');
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
}

.backgroundbox img {
  max-width: 100%;
  max-height: 100%;
}
</style>
