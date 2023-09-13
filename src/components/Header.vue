<template>
    <header>
        <h1>Task Tracker</h1>
        <Button title="Add Task" color="green"/>
    </header>
</template>


<script>
import Button from './Button.vue';
export default 
{
    name: "Header", 
    components:
    {
        Button
    }
}
</script>

<style scoped>
header
{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 30px;
}
</style>