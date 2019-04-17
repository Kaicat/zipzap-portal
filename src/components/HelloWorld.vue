<template>
  <div class="hello">
    {{msg}}
  </div>
</template>

<script lang="ts">

import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  [x: string]: any;  // 用来使 this.$message 编译通过，不然报此类没有这个属性的错

  @Prop()
  public msg!: string;

  /**
   * beforeCreated
   */
  public mounted() {
      this.$message('234');
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
