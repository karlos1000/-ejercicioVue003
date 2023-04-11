<template>
    <div>
        <img src="https://pandorafms.com/blog/wp-content/uploads/2019/02/para-que-sirve-una-API-featured.png" v-bind:style="{ height: sizeH + 'px' }" />
    </div>
    <div>
        <button v-on:click="increment">Aumentar</button>
        <button v-on:click="decrement">Disminuir</button>
    </div>
</template>

<script>
import {ref } from "vue";
export default {
    name: 'Imagen',
    props: {
    },
    setup() {
        let sizeH = ref(100);
        let sizeIncrement = 10;

        const increment = () => {
            sizeH.value = sizeH.value+sizeIncrement;
        }

        const decrement = () => {
            sizeH.value = sizeH.value-sizeIncrement;
        }

        return {
            sizeH,
            increment,
            decrement
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
