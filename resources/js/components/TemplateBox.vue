<template>
    Text1: {{ text1 }}
    <br>
    Text2text: {{ text2}}
    <br>
    Text2html: <span v-html="text2"></span>
    <hr>
    <input type="submit" v-bind:value="value">
    <!-- rövid változata: -->
    <input type="submit" :disabled="btnstatus" :value="value">
    <hr>
    <input v-bind="inputAttributes"/>
    <hr>
    <h1 v-if="seeme">Megyünk már haza?</h1>
    <hr>
    <h2 :[attrname]="attrvalue">IGEN!</h2>
</template>

<script>
export default {
    name: "TemplateBox",
    data() {
        return {
            text1: "majmok bolygója",
            text2: 'hattyú <span style="color: blue">kék tóban</span>',
            value: 'Indulás haza!',
            btnstatus: true,  // le van tiltva a gomb
            inputAttributes: {
                type: "text",
                value: 12,
                class: "input input-error",
                name: "destination"
            },
            seeme: true,
            attrname: "id",
            attrvalue: "gohome"
        };
    }
}
</script>

<style scoped>

</style>
