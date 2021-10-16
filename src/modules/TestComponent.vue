<template>
  <div>
    <p class="border__blue">this is test.</p>
    {{ testData }}
  </div>
</template>

<script>
export default {
  name: "TestComponent",
  data() {
    return {
      testData: "test data",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div {
  color: red;
}

.border {
  &__blue {
    border: 1px blue soild;
    color: blue;
  }
}
</style>
