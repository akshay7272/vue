<template>
<div class="child">
<h1>Child Component Data passing</h1>
<h2>{{name}}</h2>
<h3>{{userdata.name}} and Email is : {{userdata.email}}</h3>
<button @click="getData()"> Parent Function</button>
</div>
</template>

<script>
export default {
    name: 'ChildModule',
    props: {
        name: String,
        userdata: Object,
        getData: Function,
    },
    data() {
        return {
            
            
        }
    }
}
</script>
<style scoped>
.child{
    background-color: #ff12aa;
}
</style>
