<template>
    <div>
        <h2>Parent Component</h2>
        <button @click="child = !child">Toogle button</button>
        <ChildComponent v-show="child"/>
    </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
    export default {
        name:"ParentComponent",
        components:{
            ChildComponent
        },
        data(){
            return {
                child:true
            }
        },
        beforeCreate() {
            console.log(`parent component before create hook()`);
        },
        created() {
            console.log(`parent component create hook()`);
        },
        beforeMount() {
            console.log(`parent component before mount hook()`);
        },
        mounted() {
            console.log(`parent component mounted hook()`);
        },
        beforeUpdate() {
            console.log(`parent component before update hook()`);
        },
        updated() {
            console.log(`parent component updated hook()`)
        },
        beforeUnmount(){
            console.log(`parent Component beforeUnmount hook()`);
        },
        unmounted(){
            console.log(`parent Component unmounted hook()`);
        }

    }
</script>

<style scoped>

</style>