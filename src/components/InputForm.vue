<template>
  <div class="inputField">
      <input type="text" placeholder="Input field">
      <p>Lägg till todo</p>
  </div>
</template>

<script>
export default {

}
</script>

<style>
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
}
</style>