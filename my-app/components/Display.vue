<template>
    <section class="result">
        {{ value}}
        <div class="number">
            {{ n1 }}
        </div>
    </section>
</template>

<script>

    export default {
        props: {
            value: {
                required: true,

            },
            n1: {
                required: false,
            }
        }
    }
</script>

<style scoped>

.number {
    position: absolute;
    top: 0;

    font-size: 20px;
}
.result {
    display: flex;
    position: relative;
    justify-content: end;
    align-items: center;
    width: 300px;
    height: 60px;
    padding: 10px;
    background-color: rgb(140, 146, 219);
    border: 1px solid #3a2b2b;
}
</style>