<template>
  <div v-if="moment">
    <h2>Hello! Il est {{ moment }}</h2>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      moment: null,
      interval: null,
    };
  },

  methods: {
    reLoad() {
      axios
        .get("http://localhost:3000/moment", {
          responseType: "json",
        })
        .then((response) => {
          this.moment = response.data;
          console.log(response.data);
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },

  mounted() {
    this.reLoad();
  },

  created() {
    this.interval = setInterval(() => {
      this.reLoad();
    }, 1000);
  },
  unmounted() {
    clearInterval(this.interval);
  },
};
</script>
