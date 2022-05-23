<template>
    <button @click="decrement">-</button>
    {{ number }}
    <button @click="increment">+</button>
    <button @click="number=startValue">Clear</button>
</template>

<script>

export default {
    name: "CounterButton",
    /*props: ['startv', 'min', 'max'],*/
    props: {
        startv: {
            type: Number,
            default: 0
        },
        min: {
            type: Number,
            default: 0
        },
        max: {
            type: Number,
            default: 15
        }
    },
    data() {
        return {
            number: this.startv
        };
    },
    computed: {
        startValue() {
            return this.startv;
        }
    },
    methods: {
        increment(){
            if (this.number < this.max) {
                this.number++;
            }
        },
        decrement() {
            if (this.number > this.min){
                this.number--;
            }
        }
    }
}
</script>

<style scoped>

</style>
