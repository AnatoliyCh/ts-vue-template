<template>
  <div class="v-title-bar">
    <input
      placeholder="7"
      type="password"
      v-model="text"
      @change="test"
      @input="test"
    />
    <div class="mt-2">Value: {{ text }}</div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class vInputPassword extends Vue {
  @Prop() readonly value!: string;

  text: string = "";

  test() {
    console.log(this.text);
  }
}
</script>

<style scoped lang="scss">
.v-input-password {
}
</style>
