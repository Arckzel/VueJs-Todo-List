<template>
    <div class="tile flex-centered centered" :class="{checked: todo.checked}">
        <div class="tile-icon">
            <i class="icon" :class="todo.checked ? 'icon-check' : 'icon-time'"></i>
        </div>
        <div class="tile-content">                
            <p class="tile-subtitle">{{todo.description}}</p>
        </div>
        <div class="tile-action">
            <button @click="$emit('toggle',todo)" class="btn btn-link">
                <span v-if="todo.checked === true">Desmarcar</span>
                <span v-else>Concluido</span>

                </button>
            <button @click="$emit('remover',todo)" class="btn btn-link"><span class="text-error">Remover</span></button>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        todo: {type: Object, required: true}
    }
}
</script>

<style scoped>
    p{
        line-break: anywhere;
    }
    .tile{
        background-color: rgba(140, 217, 240, 0.274);
        margin-bottom: 20px;
        padding: 0px 5px 2px 10px;
        border-radius: 20px;
        /* padding-bottom: ; */
    }
    .tile-subtitle{
        margin: 10px 0px 0px 0px;
    }
    .tile-content{
        padding-bottom: 2px;
        margin-bottom: 5px;
    }

    .checked{
        text-decoration: line-through;
        color: gray;
    }
</style>