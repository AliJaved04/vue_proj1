<template>
<div :class="[task.remainder?'remainder': '', 'task']">
    <h3>
        {{ task.text }}
        <i class="fas fa-times" @click="deleteTask(task.id)"></i>
    </h3>
    <p>{{ task.day }}</p>
</div>
</template>

<script>
export default
{
    name:"Task", 
    props:
    {
        task: Object
    }, 

    methods:
    {
        deleteTask(id)
        {
            this.$emit('delete-task', id);
        
        }
    }
} 

</script>


<style scoped>
.task
{
   max-height: 80px;
  background-color: #f4f4f4;
  margin: 5px;
  padding:   1px 20px ;
  cursor: pointer;
}

.fas 
{
    color:  red;
}

.task.remainder
{
    border-left: 5px solid green
}
.task h3
{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>