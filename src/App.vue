<template>
  <div id="app">
    <JwInput
      name="id"
      type="text"
      placeholder="ID 를입력하세요."
      v-model="input.id"
    />
    <JwInput
      name="password"
      type="password"
      placeholder="Password 를입력하세요."
      v-model="input.password"
    />
    <Login @click="clickBtn"/>
  </div>
</template>

<script>
import Login from "@/components/Login";
import JwInput from "@/components/JwInput";
export default {
  name: 'App',
  data() {
    return {
      input: {
        id:'',
        password:'',
      },
    };
  },
  components: {
    JwInput,
    Login,
  },
  methods: {
    clickBtn(){
      console.log(`id: ${this.input.id}이고, password: ${this.input.password}이다.`);
    },
  },
}
</script>

<style>

</style>
