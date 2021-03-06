<template>
    <form>
        <input type="text" placeholder="Nouvelle tâche ..." >
        <input type="button" value="+" @click="addItem()">
    </form>
</template>
<script>
export default {
  name: 'new-todo',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    div
    {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    input
    {
      margin: 0 50px;
    }

</style>
