<template>
  <div>
      <div class="title">
          <slot name="title"></slot>
          <span>
              <slot name="subTitle"> the Subtitle</slot>
          </span>
      </div>
      <hr>
      <div>
          <slot name="content"></slot>
      </div>
      <hr>
      <div>
          <slot></slot>
      </div>
  </div>
</template>

<script>
export default {
props: {
    quote: {
        type: String
    }
}
}
</script>

<style scoped>
div {
    border: 1px solid greenyellow;
    box-shadow: 1px 1px 2px green;
    padding: 30px;
    text-align: center;
}
h2 {
    font-size: 20px;
    font-weight: 500;
    color: blueviolet;
}

.title {
    background-color: palevioletred;
}

span {
    border: 2px dashed rebeccapurple;
}
</style>