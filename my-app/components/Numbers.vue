<template>
    <section class="buttons">
        <button @click="($e) => $emit('onChange', 1)"> 1 </button>
        <button @click="($e) => $emit('onChange', 2)"> 2 </button>
        <button @click="($e) => $emit('onChange', 3)"> 3 </button>
        <button @click="($e) => $emit('onClean')"> C </button>
        <button @click="($e) => $emit('onChange', 4)"> 4 </button>
        <button @click="($e) => $emit('onChange', 5)"> 5 </button>
        <button @click="($e) => $emit('onChange', 6)"> 6 </button>
        <button></button>
        <button @click="($e) => $emit('onChange', 7)"> 7 </button>
        <button @click="($e) => $emit('onChange', 8)"> 8 </button>
        <button @click="($e) => $emit('onChange', 9)"> 9 </button>
        <button></button>
        <button @click="($e) => $emit('onChange', 0)">0</button>
    </section>
</template>

<style scoped>
.buttons {
    width: 240px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin-top: 10px;
    border: 1px solid #3a2b2b;
    background-color: rgb(214, 217, 218);
    justify-content: center;
}

.buttons button {
    margin: 0px;
    padding: 0px;
    width: 60px;
    height: 60px;
    border: 1px solid #9c8383;
    background: white;
    background-color: rgb(214, 217, 218);
}

.buttons button:hover {
    transition: 0.2s ease-in-out;
    background-color: rgb(187, 195, 197);
    cursor: pointer;
}
</style>