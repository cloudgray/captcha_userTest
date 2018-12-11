<template lang="html">
  <div class="clearAllContainer">
    <span class="accuracy">Accuracy: {{accuracy}} %</span>
    <br />
    <br />
    <span class="clearAllBtn" @click="clearTodo">Clear All</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      accuracy: 100,
    }
  },
  methods: {
    clearTodo() {
      this.$emit('removeAll');
    }
  }
}
</script>

<style lang="css" scoped>
.ClearAllContainer {
  width: 8.5rem;
  height: 50px;
  line-height: 50px;
  background-color: white;
  border-radius: 5px;
  margin: 0 auto;
}

.clearAllBtn {
  color: #e20303;
  display: black;
}
.accuracy {
  font-weight: bold;
}
</style>
