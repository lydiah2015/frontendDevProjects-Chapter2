<script>
export default {
    data() {
        return {
            organization: {
                name: 'ABC',
                employees: [
                    'Jack', 'Jill'
                ]
            },
        }
    },

    //observing all keys in the organization for changes
    // watch: {
    //     organization: {
    //         hander(v) {
    //             this.sendIntercomData()
    //         },
    //         deep: true,
    //         immediate: true,
    //     }
    // },

    // observing a specific key (name) inside the organization for changes

    watch:{
        'organization.name':{
            handler:function(v) {
                this.sendIntercomData()
            },
            immediate:true,
        }
    }
}
</script>