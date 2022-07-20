<template>
  <section>
    <FriendNav/>
    <FriendForm/>
  </section>

</template>

<script>
import FriendNav from "./components/Friend-Nav.vue";
import FriendForm from "./components/Friend-Form.vue";

export default {
  components: {
    FriendNav,
    FriendForm,
  },
};
</script>

<style>
#app {
  font-family: serif;
  /* border: 2px solid rgb(238, 21, 58); */
  width: 50%;
  margin: auto;
  padding: 20px;
}
</style>
