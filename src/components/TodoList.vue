<template>
<div id="listContainer">
    <div v-for="task in tasks" :key="task.id" id="tasklist">
        <div>
            <input type="radio" class="radio">
            <p>{{task.task}}</p>
        </div>
        <button @click="removeElement(index)">-</button>
    </div>
</div>
</template>

<script>
export default {
  name: 'todo_list',
  methods:
  {
    addElement: function ()
    {
        console.log('Element created');
    },
    removeElement: function (index)
    {
        this.tasks.splice(index, 1);
        console.log('Element deleted');
        this.tasks.push();
    },
  },
    data() {
    return {
      tasks: [
        { task: 'Premier' },
        { task: 'Deuxième' },
        { task: 'Troisième' },
        { task: 'Quatrième' },
        { task: 'Cinquième' },
        { task: 'Sixième' }
      ]
    };
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#listContainer
{
    display: flex;
    align-items: center;
    flex-direction: column;

}

#listContainer div
{
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row;
    margin: 10px 50px;
    width: 70%;
}

#tasklist
{
    width: 70%;
}
p
{
    justify-self: flex-start;
}


input[type=radio]
{
    border: 1px;
    width: 40px;
    height: 40px;
    margin: 0 10% 0 0;
}
</style>
