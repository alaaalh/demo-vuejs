<template>
  <button @click="importData">GET DATA</button>
  <div v-if="!isLoading">Loading...</div>
  <p v-else-if="isLoading && (!result || result.length === 0)">No data store</p>
  <div v-else-if="isLoading && (result || result.length > 0)">
  <div v-for="data in result" :key="data">
    <h3>{{ data.name }}</h3>
    <p>{{ data.password }}</p>
  </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      result: [],
      isLoading: true,
    };
  },
  methods: {
    importData() {
      this.isLoading = false;
      fetch(
        "https://vue-http-demo-dd166-default-rtdb.firebaseio.com/serveys.json"
      )
        .then((res) => {
          if (res.ok) {
            return res.json();
          }
        })
        .then((data) => {
          this.isLoading = true;
          console.log(data);
          const result = [];
          for (var id in data) {
            result.push({
              id: id,
              name: data[id].name,
              password: data[id].password,
            });
          }
          this.result = result;
          console.log(this.result);
        });
    },
  },
  mounted() {
    this.importData();
  },
};
</script>
