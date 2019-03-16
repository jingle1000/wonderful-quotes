<template>
    <div>
        <input type="textarea" class="form-control" v-model="quoteText">
        <button class="btn btn-primary btn-block mt-3" @click="createNew">Add New Quote</button>
    </div>
</template>

<script>
export default {
    name: "NewQuote",
    data: function() {
        return {
            quoteText: ""
        }
    },
    methods: {
        createNew() {
            this.$emit("addQuote", this.quoteText)
            this.quoteText = ''
        }
    }
}
</script>