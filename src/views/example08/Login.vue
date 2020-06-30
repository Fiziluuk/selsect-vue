<template>
  <div id = "divcss5">
    <form ref="form">
      <br />
      <input type="text" v-model="number" />
      <br />
      <input type="password" v-model="password" />
      <br />
      <button type="button" @click="submit">login</button>
    </form>
    <!-- {{ number }} -->
  </div>
</template>
<script>
import { ISLOGIN } from "@/store/types.js";
import { mapState } from "vuex";
export default {
  data: () => ({
    number: null,
    password: null
  }),
  methods: {
    submit() {
      this.$store.dispatch(ISLOGIN, {
        number: this.number,
        password: this.password
      });
      this.$refs.form.reset();
    }
  }
};
</script>
<style scoped>
h1 {
  color: blue;
}
ul {
  margin-top: 20px;
  margin-left: 30px;
}
ul ul {
  margin-top: 00px;
}
ul > li {
  margin-left: 10px;
}
body{ text-align:center} 
#divcss5{margin:0 auto;border:1px solid #000;width:300px;height:100px}
</style>
