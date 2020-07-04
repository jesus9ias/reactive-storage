<template>
  <div class="home">
    Clicks {{ count }}
    <button @click="update">Click me</button>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    update() {
      this.count += 1;
      localStorage.setItem('count', this.count);
    },
  },
  created() {
    this.count = Number(localStorage.getItem('count'));
  },
};
</script>
