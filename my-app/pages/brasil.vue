<template>
    <ul>
        <li>Nome Comum: {{ this.dados[0].name.nativeName.por.common }}</li>
        <li>Nome Oficial: {{ this.dados[0].name.nativeName.por.official }}</li>
        <li>Moeda: {{ this.dados[0].currencies.BRL.name}}</li>
        <li>Simbolo da Moeda: {{ this.dados[0].currencies.BRL.symbol}}</li>
        <li>Capital: {{this.dados[0].capital[0]}}</li>
        <li>Regiao: {{ this.dados[0].region}}</li>
        <li>Sub-Regiao: {{ this.dados[0].subregion}}</li>
        <li> Fronteiras: </li>
        <ul v-for="border in this.dados[0].borders">
            <li >
                {{ border }}
            </li>
        </ul>
    </ul>
</template>

<script>
    import dados from "~/brasil.json";

    export default {
        data() {
            return {
                dados: dados,
            }
        }

    }
</script>