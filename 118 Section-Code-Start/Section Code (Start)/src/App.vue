<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
          <button @click="selectedComponent = 'appQuote'">Quote</button>
          <button @click="selectedComponent = 'appAuthor'">Author</button>
          <button @click="selectedComponent = 'appNewComponent'">New</button>
          <hr>
          <p>Selected component: {{selectedComponent}}</p>
          <keep-alive>
              <component :is="selectedComponent"></component>
          </keep-alive>

        <!-- <appQuote>
          <h2 slot="title">{{quoteTilte}}</h2>
          <p slot="content">{{quote}}</p>
        </appQuote> -->
      </div>
    </div>
  </div>
</template>

<script>
import QuoteCopmopnent from "./components/Quote.vue";
import Author from "./components/Author.vue";
import NewComponent from "./components/NewComponent.vue";

export default {
  data: () => ({
      quoteTilte: "the quote is under",
      quote: "A wonderful quote!",
      selectedComponent: "appQuote"
  }),
  components: {
    appNewComponent: NewComponent,
    appQuote: QuoteCopmopnent,
    appAuthor: Author
  }
};
</script >

<style scoped>
div {
  padding: 30px;
}
</style>
