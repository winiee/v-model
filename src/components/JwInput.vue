<template>
  <div>
    <input
      :type="type"
      :name="name"
      :placeholder="placeholder"
      v-model="newValue"
     />
  </div>
</template>

<script>
export default {
  name: "JwInput",
  props: {
    placeholder: {
      type: String,
      default: '',
    },
    name: {
      type: String,
      default: '',
    },
    type:{
      type:String,
      default:"text",
    },
    value:null,
  },
  computed:{
    newValue: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit('input', val);
      },
    },
  },
};
</script>

<style scoped>

</style>