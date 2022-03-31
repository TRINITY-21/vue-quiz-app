<script>

export default {
    data(){
        return {
            ages:"1"
        }
    },

    props:{
        age:{
            type:[Number]
        }
    },

    emits:["age-change"],

    methods: {
        updateAge(){
            this.$emit("age-change", 2)
        }
    },
}


</script>


<template>
    <h1 v-if="age>30"> I am {{age}} years old</h1>

    <h3 v-else>Hello age is changed {{age}} </h3>
    <button @click="updateAge">update</button>

</template>