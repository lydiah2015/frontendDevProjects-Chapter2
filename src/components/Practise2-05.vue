<template>
    <button @click="getDate">Click Me</button>
    <div>{{ animals }}</div>
    <div class="contain">
        <button @click="getNewName()">Click to generate name</button>
        <p v-if="author">{{ author }}</p>
    </div>
</template>
<script>
export default {
    data() {
        return {
            // animalList: ['dog', "cat"],
            author: '',
        }
    },
    computed: {
        // animals() {
        //     return this.animalList.slice(1)
        // },
    },
    methods: {
        getDate() {
            alert(Date.now())
        },
        async getNewName() {
            await fetch('https://randomuser.me/api/').then(response => response.json()).then(data => {
                this.author = data.results[0].name
            })
        }
    },
    watch: {
        author: function (newVal, oldVal) {
            this.author = newVal.first
            alert(`Name changed from ${oldVal.first} to ${newVal.first} `)
        }
    }
}
</script>
<style>
.contain{
    margin-top: 15px;
    margin: 15px;

}
</style>