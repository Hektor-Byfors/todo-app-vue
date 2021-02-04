<template>
  <ul class="ul-list">
   <li>
        <button v-on:click="toggleShowCheck()" v-bind:class="{ checked: checked }"><span class="material-icons">done</span></button>
        <p>Köttbullar</p>
        <span v-on:mouseover="toggleHoverRemove()" v-on:mouseleave="toggleHoverRemove()" v-bind:class="{ hoverRemove: hoverRemove }" class="material-icons removeLi">clear</span>
    </li>
    <li>
        <button v-on:click="toggleShowCheck()" v-bind:class="{ checked: checked }"><span class="material-icons">done</span></button>
        <p>Köttbullar</p>
        <span v-on:mouseover="toggleHoverRemove()" v-on:mouseleave="toggleHoverRemove()" v-bind:class="{ hoverRemove: hoverRemove }" class="material-icons removeLi">clear</span>
    </li>
    <li>
        <button v-on:click="toggleShowCheck()" v-bind:class="{ checked: checked }"><span class="material-icons">done</span></button>
        <p>Köttbullar</p>
        <span v-on:mouseover="toggleHoverRemove()" v-on:mouseleave="toggleHoverRemove()" v-bind:class="{ hoverRemove: hoverRemove }" class="material-icons removeLi">clear</span>
    </li>
  </ul>
</template>

<script>
export default {
    data() {
    return {
        checked: false,
        hoverRemove: false
    }
},
methods: {
    toggleShowCheck() {
        this.checked = !this.checked
    },
    toggleHoverRemove() {
        this.hoverRemove = !this.hoverRemove
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

li .hoverRemove {
    background-color: rgb(155, 155, 155);
}
</style>