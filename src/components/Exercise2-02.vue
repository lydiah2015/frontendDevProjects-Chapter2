<script>
export default {
data () {
    return {
        count : -1,
        divideByTwo:0,

    }
},
computed: {
    incrementOne : {
        //getter
        get(){
            return this.count +1
        },

        //setter
        set(val){
            this.count = val -1
            this.divideByTwo = val/2
        },
    },
},
}
</script>
<template>
    <h3>testing exercise2</h3>
    <div class="container">
        <input type="number" placeholder="Input Number" v-model="incrementOne">
        <h3>Get Input: {{ incrementOne }}</h3>
        <h5>Set Division : {{ divideByTwo }}</h5>
    </div>
</template>