<template>
    <p class="infop">Du har <span>{{ todoListings.length }}</span> todos kvar i listan</p>

    <ul class="ul-list">
        <li v-for="(list, index) in todoListings">
            <button
            v-bind:class="{ checked: list.checked }"
            v-on:click="toggleShowCheck(list)"
            >
            <span class="material-icons">done</span>
            </button>
            <p>{{ list.todoItem }}</p>
            <span 
            class="material-icons removeLi"
            v-on:click="removeTodo(index)"
            >
            clear
            </span>
        </li>
    </ul>

    <div class="inputField">
        <input type="text" placeholder="Potatismjöl" v-model="newTodo">
        <p v-on:click="addTodo()">Lägg till</p>
    </div>
</template>

<script>
export default {
   data() {
    return {
        newTodo: 'Ketchup',
        todoListings: [
            {todoItem: 'Köttbullar', checked: false},
            {todoItem: 'Makaroner', checked: false}
        ]
    }
},
methods: {
    toggleShowCheck(list) {
        list.checked = !list.checked
    },
    addTodo() {
        if(this.newTodo.trim().length == 0) {
            this.newTodo = ''
            return
        }
        this.todoListings.push ({
            checked: false,
            todoItem: this.newTodo
            })

            this.newTodo = ''
    },
    removeTodo(index) {
        this.todoListings.splice(index, 1)
    }
}
}
</script>

<style>
.ul-list {
    list-style-type: none;
    width: 370px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    margin: 0 0 15px 0;
    padding: 0;
}

.ul-list li {
    height: 60px;
    background-color: rgb(199, 199, 199);
    display: flex;
    align-items: center;
    margin-bottom: 6px;
    border-radius: 2px;
}

li button .material-icons {
    color:  rgb(95, 95, 95);
    font-size: 28px;
    font-weight: 600;
}

.ul-list p {
    color: rgb(58, 58, 58);
    font-weight: 500;
}

.ul-list button {
    height: 34px;
    width: 34px;
    background-color: rgb(95, 95, 95);
    border-radius: 50%;
    outline: none;
    border: none;
    margin: 0 13px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: 500ms;
}

.removeLi {
    color: rgb(88, 88, 88);
    font-weight: 500;
    font-size: 25px;
    position: absolute;
    height: 30px;
    width: 30px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 323px;
    transition: 500ms;
    cursor: pointer;
    box-shadow: inset 0px 0px 10px 2px rgb(199, 199, 199);
}

li .checked {
    background-color: rgb(228, 228, 228);
    transition: 500ms;
}

li .removeLi:hover {
    background-color: rgb(155, 155, 155);
}

.inputField {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 370px;
    margin-bottom: 15px;
}

input {
    width: 366px;
    padding: 0;
    border: 0;
    height: 58px;
    border: 2px solid rgb(34, 34, 34);
    border-style: solid solid none solid;
    outline: none;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 15px;
    font-weight: 600;
    text-align: center;
    color:   rgb(34, 34, 34);
}

::placeholder {
    color: rgb(179, 179, 179);
}

.inputField p {
    width: 100%;
    border-radius: 0;
    background-color: rgb(34, 34, 34);
    color: white;
    font-weight: 600;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 60px;
    cursor: pointer;
}
</style>