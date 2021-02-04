<template>
    <HeaderIcon />
    <TodoList />
</template>

<script>
import HeaderIcon from './HeaderIcon.vue'
import TodoList from './TodoList.vue'

export default {
    components: {
        HeaderIcon,
        TodoList
    }
}
</script>

<style scooped>
    .infop {
       font-weight: 500;
       color: rgb(58, 58, 58);
    }

    span {
        font-weight: 900;
        font-family: sans-serif;
    }
</style>