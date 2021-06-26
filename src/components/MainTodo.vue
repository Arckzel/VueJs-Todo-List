<template>
    <div class="todo container grid-xs py-2">
        <img class="img-responsive img-logo" alt="Vue logo" src="@/assets/logo.png">   
        <form @submit.prevent="addTodo(todo)">
            <div class="input-group">
                <input class="form-input" v-model="todo.description" type="text" placeholder="Novo todo">
                <button class="btn btn-primary input-group-btn">Adicionar</button>
                
            </div>
        </form>
        <div class="todo-list">
            <ObjectTodo v-for="t in todos" :key="t.id" :todo="t" @toggle="toggleTodo" @remover="removerTodo"/>
        </div>        
    </div>  
</template>

<script>
import ObjectTodo from './ObjectTodo.vue';
export default {    
    name: 'MainTodo',
    components: { ObjectTodo },
    data(){
        return {  todos: [], todo: { checked: false }  };
    },
    methods: {
        addTodo(todo){
            console.log(this.todo);
            todo.id = Date.now();
            this.todos.push(todo);      
            this.todo = {checked: false};
        },

        toggleTodo(todo){
            const index = this.todos.findIndex(item => item.id === todo.id);
            if(index > -1){
                const checked = !this.todos[index].checked;
                this.todos[index].checked = checked;
                console.log(this.todos[index]);
            }
        },
        removerTodo(todo){
            const index = this.todos.findIndex(item => item.id === todo.id);
            if(index > -1){
                this.todos.pop(index);
            }
        }
    }
}
</script>

<style scoped>
.img-logo{
  max-width: 100px !important;
  margin: 0 auto; 
  padding: 10px 0; 
}
button{
    margin: 0 5px !important;
}
.todo-list{
    padding-top: 2rem;
}

</style>