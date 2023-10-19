<script>
export default{
    watch: {
        myDataProperty: {
            handler: function(newVal, oldVal){
                console.log('MyDataProperty changed:', newVal, oldVal)
            },
            immediate:true,
            deep:true

        },
    }
}
</script>