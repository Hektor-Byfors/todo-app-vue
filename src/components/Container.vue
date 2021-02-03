<template>
    <HeaderIcon />
    <p class="infop">Du har <span>3</span> todos kvar att göra</p>
    <TodoList />
    <InputForm />
</template>

<script>
import HeaderIcon from './HeaderIcon.vue'
import TodoList from './TodoList.vue'
import InputForm from './InputForm'
export default {
    components: {
        HeaderIcon,
        TodoList,
        InputForm
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