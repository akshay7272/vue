<template>
    
    <button @click="GetUserr(name)">get username </button>
</template>

<script>

export default {
    name:'ChildtoParent',
    data() {
        return {
            name:'Shivam Madan',
        }
    },
    props: {
        GetUserr:Function,
    }
}
</script>