<template>
    <main>
        <Display :value="display" :n1="n1" />
        <Numbers @onChange="onChange" @onClean="onClean" />
        <Actions @onSubtract="onSubtract" @onAdd="onAdd" @onResult="onResult" @onMultiply="onMultiply" @onDivision="onDivision" />
    </main>
</template>

<script>

export default {
    data() {
        return {
            display: "",
            n1: "",
            math: ""
        }
    },
    methods: {
        onChange(number) {
            if(this.math === "result"){
                this.display = "";
                this.n1 = "";
            }

            String(this.display);
            this.display = parseInt(this.display + String(number));
        },
        onAdd() {
            this.n1 = this.display;
            this.display = "";
            this.math = "plus";
        },
        onSubtract() {
            this.n1 = this.display;
            this.display = "";
            this.math = "minus";
        },
        onMultiply() {
            this.n1 = this.display;
            this.display = "";
            this.math = "multiply";
        },
        onDivision() {
            this.n1 = this.display;
            this.display = "";
            this.math = "division";
        },
        onResult() {
            if(this.math === "plus") {
                this.display = this.n1 + this.display;
            }
            else if (this.math === "minus") {
                this.display = this.n1 - this.display;
            }
            else if (this.math === "division") {
                this.display = this.n1 / this.display;
            }
            else if (this.math === "multiply") {
                this.display = this.n1 * this.display;
            }
            this.math = "result";
        },
        onClean() {
            this.display = "";
            this.n1 = "";
        }
    }

}
</script>

<style>
* {
    font-size: 30px;
}

main {

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin: auto;
    width: 370px;
    height: 450px;
    background-color: rgb(243, 241, 241);
    border: 2px dotted #000;
}
</style>