<template>
    <div>
        <h2>Child Component</h2>
    </div>
</template>

<script>
    export default {
        name:"ChildComponent",
        beforeCreate() {
            console.log(`child component before create hook()`);
        },
        created() {
            console.log(`child component create hook()`);
        },
        beforeMount() {
            alert('you are mounting child component');
            console.log(`child component before mount hook()`);
        },
        mounted() {
            console.log(`child component mounted hook()`);
        },
        beforeUpdate() {
            console.log(`child component before update hook()`);
        },
        updated() {
            console.log(`child component updated hook()`);
        },
        beforeUnmount(){
            alert("you are unmounting childComponent");
            console.log(`child component beforeUnmount hook()`);
        },
        unmounted(){
            alert("you are unmounted childComponent");
            console.log(`child component unmounted hook()`);
        }
    }
</script>

<style scoped>

</style>