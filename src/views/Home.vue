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
      count: localStorage.getItem('count'),
    };
  },
  methods: {
    update() {
      const count = Number(localStorage.getItem('count'));
      localStorage.setItem('count', count + 1);
    },
  },
};
</script>
