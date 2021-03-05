<template>
        <header>
          <p class="placeholder">{{DateTime()}}</p>
          <p class="placeholder" id="title">Exercice VueJS TodoList</p>
          <p class="placeholder">{{tasks.length + ' Tâche(s)'}}</p>      
        </header>
</template>

<script>
export default {
  name: 'todo-header',
  methods: 
  {
     DateTime()
     {
      var current = new Date;
      var weekday = new Array(7);
        weekday[0]="Lundi";
        weekday[1]="Mardi";
        weekday[2]="Mercredi";
        weekday[3]="Jeudi";
        weekday[4]="Vendredi";
        weekday[5]="Samedi";
        weekday[6]="Dimanche";
      var month = new Array(12);
        month[0]="Janvier";
        month[1]="Février";
        month[2]="Mars";
        month[3]="Avril";
        month[4]="Mai";
        month[5]="Juin";
        month[6]="Juillet";
        month[7]="Août";
        month[8]="Septembre";
        month[9]="Octobre";
        month[10]="Novembre";
        month[11]="Décembre";
        const CurrentDate = `${weekday[current.getDay()]} ${current.getDate()} ${month[current.getMonth()]}`;
        return CurrentDate;
    },

    tasks()
    {
      return null;
    }
  },
  props: {
    msg: String
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    header
    {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: row;
        margin: 10px 50px;
      border-radius: 40px;
    }
    p:nth-child(2)
    {
      color: rgb(0, 255, 179);
    }
    p
    {
      font-weight: bold;
    }

</style>
