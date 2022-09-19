<!-- <template>
  <div v-if="times">
    <h2>Hello! Il est {{ times.timeline }}</h2>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from "axios";

export default {
  name: "HomeView",

  data() {
    return {
      times: null,
      intervalID: null,
    };
  },

  methods: {
    newCall() {
      axios
        .get("http://localhost:3000/api/time", {
          responseType: "json",
        })
        .then((response) => {
          this.times = response.data;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },

  mounted() {
    this.newCall();
  },

  created() {
    this.intervalID = setInterval(() => {
      this.newCall();
    }, 3000);
    console.log(this.newCall);
  },
};
</script> -->

<!-- 
<template>
    <h2>Hello! Il est {{ moment(new Date()).format("HH:mm:ss") }}</h2>
  </template>
  
  <script>
  // @ is an alias to /src
  import moment from "moment";
  
  export default {
    name: "HomeView",
  
    data() {
      return {
        times: null,
        moment: moment,
      };
    },
  };
  </script> -->
