<template>
<h1>{{data.name}}</h1>
<h4>{{data.email}}</h4>
<button @click="nameData(data.name)">get name</button>
</template>

<script>
export default {
    name: 'NewChild',
    props: {
        data: Object,
        nameData: Function,

    },
    data() {
        return {

        }
    }

}
</script>
