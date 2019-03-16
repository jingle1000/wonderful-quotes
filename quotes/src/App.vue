<template>

  <div id="app">
    <navbar></navbar>
    <div class="container">
      <div class="pt-4">
        <progress-bar :quotes=quotesLength :maxQuotes=maxQuotes></progress-bar>
      </div>
      <div class="card m-4 p-4 shadow">
        <quote-form @addQuote="newQuote"></quote-form>
      </div>
      <div class="p-4 m-3">
        <quote-grid :quotes=quotes @deleteQuote="removeQuote"></quote-grid>
      </div>
      <div class="alert alert-primary">click quote to delete</div>
    </div>
  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid.vue"
  import Nav from "./components/Nav.vue"
  import ProgressBar from './components/ProgressBar.vue'
  import NewQuote from './components/NewQuote.vue'
  export default {
    name: "app",
    components: {
      quoteGrid: QuoteGrid,
      navbar: Nav,
      progressBar: ProgressBar,
      quoteForm: NewQuote,
    },
    data: function () {
      return {
        quotes: ["Sample Quote"],
        maxQuotes: 10,
      }
    },
    methods: {
      newQuote(quote) {
        this.quotes.push(quote)
      },
      removeQuote(index) {
        this.quotes.splice(index, 1);
      }
    },
    computed: {
      quotesLength: function() {
        return this.quotes.length
      }
    }
  }
</script>

<style>


</style>