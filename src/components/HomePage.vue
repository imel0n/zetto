<template>
  <button @click="handleLogout">Log Out</button>
</template>

<script>
export default {
  methods: {
    handleLogout() {
      console.log("attempting logout");
      this.$router.push("/");
    }
  }
}
</script>

<style scoped>
</style>