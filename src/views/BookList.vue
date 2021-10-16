<template>
  <div>
    <h1>List of Books.</h1>
    <ul>
      <li v-for="book in books" :key="book.id" @click="showBookDetail(book.id)">
        {{ book.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "BookList",
  data() {
    return {
      bookIndex: -1,
      books: [
        { id: 1, title: "aaaaaaa", content: "dddddddd" },
        { id: 2, title: "bbbbbbb", content: "eeeeeeee" },
        { id: 3, title: "ccccccc", content: "ffffffff" },
      ],
    };
  },
  methods: {
    showBookDetail(id) {
      this.bookIndex = id - 1;
      this.$router.push({
        name: "Book",
        params: {
          id: this.books[this.bookIndex].id,
          title: this.books[this.bookIndex].title,
          content: this.books[this.bookIndex].content,
        },
      });
    },
  },
};
</script>

<style></style>
