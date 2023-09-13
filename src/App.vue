<template>
  <div class="container">
    <Header/>
    <Tasks  :tasks="tasks"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';
export default {
  name: 'App',
  components: {
   Header, Tasks
  },
  data()
  {
    return 
    {
      tasks : []
    }
  },

  methods:
  {
   
  },

  
  created()
  {
    this.tasks = [
      {id:1, text:"Doctors Appointment",  day:"March 1st at 2:00 PM",remainder :true, },
      {id:2, text:"Meeting at School",  day:"March 5st at 1:00 PM",remainder :false, },
      {id:3, text:"Cleaning the Appartment",  day:"March 6st at 6:00 PM",remainder :true, },
    ]
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato&display=swap");
body
{
  font-family: Lato;

}


.container
{

  max-width: 500px;
  min-height: 300px;
  margin: 30px auto;
  padding: 30px;
  overflow: auto;
  border: 1px solid steelblue;
}

.btn
{
  background-color: black;
  color: white;
  padding: 10px;
  font-family: Lato;
  font-weight: 500;
  font-size: 1.0rem;
  border-radius: 7px;
}
</style>
