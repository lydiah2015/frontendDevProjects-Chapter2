<script>
export default{
data(){
    return{
        firstName:'',
        lastName:'',

    }
},
computed:{
fullName(){
    return `${this.firstName} ${this.lastName}`
}
},
}
</script>
<template>
        <h2>Exercise2-01</h2>

<div class="btm-body">
<input type="text" placeholder="First name" v-model="firstName" >
<input type="text" placeholder="Last name"  v-model="lastName">
</div>
<h3 class="output">{{ fullName }}</h3>

</template>
<style>
.btm-body{
    display: flex;
    justify-content: space-around;
    /* margin-left: 15px;
    margin-right: 15px; */
    
}
</style>