<script>
const obj = {
    get example() {
        return 'Getter'
    }
}
console.log(obj.example)

const obj1 = {
    set example1(value) {
        this.information.push(value)
    },
    information: []
}
obj1.example1 = 'hello '
obj1.example1 = 'world'

console.log(obj1.information)
export default {
    data() {
        return {
            count: 0,
        }
    },
    method:{
        callAnotherApi (){
            // do something
        }
    },
    computed: {
        myComputedDataProp: {
            get() {
                return this.count + 1
            },
            set(value) {
                this.count = value - 1
                this.callAnotherApi(this.count)

            },


        }
    }
}


</script>
<template></template>
<style></style>