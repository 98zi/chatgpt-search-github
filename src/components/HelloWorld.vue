<template>
  <h1>ChatGPT Search Github</h1>

  <div class="input-wrap">
    <input
      type="text"
      placeholder="Start searching GitHub repositories via ChatGPT..."
      class="input input-bordered w-full max-w-xs"
    />
    <button class="btn btn-neutral" @click="submit">Search</button>
  </div>

  <ul>
    <li></li>
  </ul>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    submit() {
      console.log(1);
      fetch("https://worker-dark-math-9356.anghunk.workers.dev/search?q=vue")
        .then((response) => response.json())
        .then((data) => console.log(data));
    },
  },
};
</script>

<style scoped>
h1 {
  margin: 2em 0;
  text-align: center;
  font-size: 2rem;
}

.input-wrap {
  width: 100%;
  max-width: 600px;
  display: flex;
  margin: 0 auto;
}

.input {
  flex: 1;
  margin-right: 10px;
}
</style>
