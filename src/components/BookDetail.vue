<template>
  <div>
    <p>BookDetail</p>
    <p>title : {{ title }}</p>
    <p>content: {{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "BookDetail",
  props: {
    id: Number,
    title: String,
    content: String,
  },
  data() {
    return {
      bookIndex: this.$route.params.id - 1,
    };
  },
};
</script>

<style></style>
