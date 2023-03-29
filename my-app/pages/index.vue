<template>
    <main>
        <Display :value="display" :n1="n1" :n2="n2" :math="math" />
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
            n2: "",
            math: ""
        }
    },
    methods: {
        onChange(number) {
            if(this.math === "result"){
                this.display = "";
                this.n1 = "";
                this.n2 = "";
            }
            String(this.display);
            this.display = parseInt(this.display + String(number));
        },
        onAdd() {
            this.n1 = this.display;
            this.display = "";
            this.math = "+";
        },
        onSubtract() {
            this.n1 = this.display;
            this.display = "";
            this.math = "-";
        },
        onMultiply() {
            this.n1 = this.display;
            this.display = "";
            this.math = "*";
        },
        onDivision() {
            this.n1 = this.display;
            this.display = "";
            this.math = "/";
        },
        onResult() {
            this.n2 = this.display;
            this.display = "";
            if(this.math === "+") {
                this.display = this.n1 + this.n2;
            }
            else if (this.math === "-") {
                this.display = this.n1 - this.n2;
            }
            else if (this.math === "/") {
                this.display = this.n1 / this.n2;
            }
            else if (this.math === "*") {
                this.display = this.n1 * this.n2;
            }
            this.math = "result";
        },
        onClean() {
            this.display = "";
            this.n1 = "";
            this.n2 = "";
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