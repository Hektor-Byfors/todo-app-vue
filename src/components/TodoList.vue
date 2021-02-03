<template>
  <ul class="ul-list">
    <li>
        <button></button>
        <p>Makaroner</p>
    </li>
    <li>
        <button></button>
        <p>Köttbullar</p>
    </li>
    <li>
        <button></button>
        <p>Mjölk</p>
    </li>
  </ul>
</template>

<script>
export default {

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
}
</style>