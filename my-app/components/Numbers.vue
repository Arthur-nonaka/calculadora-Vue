<template>
    <section class="buttons">
        <button> 1 </button>
        <button> 2 </button>
        <button> 3 </button>
        <button> 4 </button>
        <button> 5 </button>
        <button> 6 </button>
        <button> 7 </button>
        <button> 8 </button>
        <button> 9 </button>
        <button>0</button>
    </section>
</template>

<style scoped>
.buttons {
    width: 180px;
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