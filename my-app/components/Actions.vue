<template>
    <section class="actions">
        <button>+</button>
        <button>-</button>
        <button>=</button>
    </section>
</template>

<style scoped>
.actions {
    width: 180px;
    display: flex;
    flex-direction: row;
    margin-top: 10px;
    border: 1px solid #3a2b2b;
    background-color: rgb(124, 147, 155);
}

.actions button {
    margin: 0px;
    padding: 0px;
    width: 60px;
    height: 60px;
    border: 1px solid #9c8383;
    background: white;
    background-color: rgb(124, 147, 155);
}

.actions button:hover {
    transition: 0.2s ease-in-out;
    background-color: rgb(113, 141, 150);
    cursor: pointer;
}
</style>