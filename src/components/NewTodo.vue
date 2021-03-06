<template>
    <form>
        <input type="text" placeholder="Nouvelle tâche ..." id='addItem'>
        <input type="button" value="+" @click="addItem()">
    </form>
</template>
<script>
import TodoList from './TodoList';
export default {
  name: 'new-todo',
  methods:
  {
    addItem()
    {
      var TodoArr = TodoList.data().tasks;
      var newItem = document.getElementById("addItem").value;

      if(newItem =="")
      {
        console.log('Erreur : Vous devez remplir la barre de texte')
      }
      else
      {
        console.log(TodoArr);
        var FinalArr = TodoArr.unshift({task: newItem},);
        console.log(TodoArr);
        FinalArr = TodoArr;
        console.log(FinalArr)
      }
    }
  },
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
