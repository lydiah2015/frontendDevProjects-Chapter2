<script>
export default {
    data() {
        return {
            name: '',
            title: 'Mr.',
            surname: 'Smith',
            post: {
                fields: {
                    author: {
                        firstName: 'John',
                        lastName: 'Doe'
                    },
                    entries: [{
                        title: "Entry 1",
                        content: "Entry 1's content",
                        featured: true
                    },
                    {
                        title: "Entry 2",
                        content: "Entry 2's content",
                        featured: false
                    }]
                }
            }
        }
    },
    computed: {
        error() {
            return this.name ? '' : 'Name is required'
        },
        formalName() {
            return `${this.title} ${this.surname}`
        },
        fullName(){
            const{firstName, lastName} = this.post.fields.author;
            return`${firstName} ${lastName}`
        },
        totalEnteries(){
            return this.post.fields.entries.length
        },
        featuredEnteries(){
            const {entries} = this.post.fields;
            return entries.filter(entry => !! entry.featured)
        },

    }
}
</script>
<template>
    <div class="body">
        <div class="label">
            <label>Name</label>
            <input v-model="name" class="input">
        </div>
        <div class="span">
            <span>{{ error }}</span>
        </div>

        <div class="props">
            <h2>Combining Data Props</h2>

            <div>{{ formalName }}</div>
        </div>
        <div>
            <h2>
                Calculating and displaying complex information
            </h2>
            <p>{{ fullName }}</p>
            <p>{{ totalEnteries }}</p>
            <p>{{ featuredEnteries }}</p>
        </div>
    </div>
</template>
<style>
.label {
    display: flex;
    flex-direction: row;
}

.input {
    margin-left: 10px;
}

.props {
    display: flex;
    flex-direction: column;
    margin-top: 20px;
}

.body {
    display: flex;
    flex-direction: column;

}

/* span{
    color: white;
} */
</style>