<template>
  <div class="fatherClass">
    我是父组件
    <h2>{{ msg1 }}</h2>
    <!-- <h2>{{ $attrs.msg2 }}</h2>
    <h2>{{ $attrs.msg3 }}</h2>
    <h2>{{ $attrs.msg4 }}</h2> -->
    <Sun v-bind="$attrs" v-on="$listeners"></Sun>
  </div>
</template>
<script>
import Sun from "./sun/sun.vue";
export default {
  components: { Sun },
  name: "DemoFather",
  props: { msg1: { type: String, default: "" } },
  mounted() {
    console.log("fu组件实例", this);
  },
};
</script>
<style lang="less" scoped>
.fatherClass {
  width: 850px;
  height: 400px;
  background-color: #baf;
  margin-left: 50px;
  margin-top: 50px;
}
</style>
