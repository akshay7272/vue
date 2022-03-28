<template>
<div v-html="tag">
</div>
<div v-html="tag2" :class="ApllyClass">
</div>
<h1 :class="ApplyClass"> Hey Buddy Class Binding</h1>
<button @click="green1=!green1"> change class</button>

<h2> Props calling Your Name as {{name}}</h2>
</template>

<script>
export default {
    name: 'HtmlBinding',
    props: {
        name: String,
    },
    data() {
        return {
            tag: '<h1 class="Binding">Welcome Akshay Your Html Binding Working Perfectly</h1>',
            tag2: '<h2> This is the h2 tag with the help of html data Binding </h2>',
            green1: true,
        }
    },
    computed: {
        ApplyClass() {
            return {
                green: this.green1,
                err: true,
                otherclass: true,
                Binding: true
            }
        },
        ApllyClass() {
            return {
                otherclass: true
            }
        }

    },
}
</script>

<style scoped>
.Binding {
    color: rgb(3, 3, 3);
    background-color: yellowgreen;
}

.green {
    font-size: 70px;
    background-color: rgb(24, 17, 13);

}

.otherclass {
    color: green;
}

.err {
    font-family: Georgia, 'Times New Roman', Times, serif;
}
</style>
