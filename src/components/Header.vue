<template>
    <header>
        <h1 v-on:click="changeTitle">{{ title }}</h1>
    </header>
</template>
<script>
import { bus } from '../main';
export default {
    props: {
        title: {
            type: String
        }
    },
    data() {
        return {
            // if uncomment this it will duplicated title
            // title: 'Vue Practice'
        };
    },
    methods: {
        changeTitle: function() {
            //this using event (child to parent)
            // this.$emit('changeTitle', 'Vue Wizard');
            // this time we are using bus
            this.title = 'vueeeeeeeee';
            bus.$emit('titleChanged', 'vue wizards bus');
        }
    }
};
</script>
<style scoped>
header {
    background: lightgreen;
    padding: 10px;
}
h1 {
    color: #222;
    text-align: center;
}
</style>
