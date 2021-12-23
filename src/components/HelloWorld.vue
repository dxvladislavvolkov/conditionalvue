<template>
  <Comp1 opt2="4321">
    <Comp2 v-if="false"></Comp2>
  </Comp1>
</template>

<script>
import { defineComponent } from "vue";
import Comp1 from "./comp1.vue"
import Comp2 from "./comp2.vue"

export default defineComponent({
  name: "HelloWorld",
  components: {
    Comp1,
    Comp2,
  },
  props: {
    readonly: {
      type: Boolean,
      default: false
    },
  },
  created() {
    this.$_config = {
      opt1: '123'
    };
  },
  mounted() {
    console.log(this.$_config)
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
