<template>
    <div class="container-form">
        <form>
            <label for="choose">Rentrez votre tâche : </label>
            <input  v-model="formTasks.task" type="text" placeholder="Saisir ma tâche" >
            <button v-on:click.prevent="addTask()">Ajouter ma tâche</button>
        </form>
        <ul id="list">
            <li v-for="(todo, index) in todos" v-bind:key="index" class="card" v-on:click="deleteTask(index)">{{ todo }}
                <liste v:bind:todo="todo"></liste>
            </li>
        </ul>
    </div>
</template>
<script>
    import Liste from './Liste.vue'

    export default{
        name: 'AddTask',
        data(){
            return{
                formTasks: {
                    task: ''
                },
                todos:['JavaScript', 'PHP', 'VueJS', 'Mysql']
            }
        },
        components:{
            'liste' : Liste,
        },
        methods:{
            deleteTask(index){
            this.todos.splice(this.todos[index], 1);
            },
            addTask(){
                this.todos.push(this.formTasks.task);
                this.formTasks.task = "";
            }
        }
    }
</script>
<style>
    .container-form{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    form{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        width: 50%;
        margin: 30px 0 30px 0;
        text-align: center;
        box-shadow: 3px 4px 12px rgba(0,0,0,.5);
        border-radius: 5px;
        padding: 20px 30px;
    }

    label{
        display: block;
    }
    input{
        width: 80%;
        margin: 10px 0 10px 0;
        padding: 10px 20px;
        border:none;
        background:  rgba(149, 151, 153, 0.3);
    }

    button{
      padding: 10px 20px;
      background: rgba(44, 130, 201, .6); 
      border: none;
      outline: none; 
      border-radius: 5px;
    }

    button:hover{
        background: rgba(75, 119, 190, 1);
        color: #F1F1F1;
    }
     div{
        width: 100%;
    }
    #list{
        width: 100%;
      list-style-type: none;
        display: flex;
        align-items: center;
        flex-direction: column;  
    }
    .card{
        position: relative;
        width: 50%;
        padding: 20px 30px;
        box-shadow: 3px 4px 12px rgba(0,0,0,.5);
        margin: 5px 0 5px 0;
        border-radius: 5px;
    }

</style>