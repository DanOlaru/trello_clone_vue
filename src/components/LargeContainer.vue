<template>
  <div>
    {{title}}
  <el-card class="box-card">
    <div class="card-header">
      <span>Card name</span>
      <el-button class="button" type="text" @click="operation">Operation button</el-button>
    </div>
    <!-- <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div> -->
  </el-card>
  </div>
</template>

<script>
export default {
  name: 'LargeContainer',
  props: {
    title: String
  },

  data () {
    return {

    }
  },

  methods: {
    operation () {
      console.log('OPPERATIONs')
    }
  },

  mounted () {
    console.log('TWAS MOUNTED ' + JSON.stringify(this.title))
  }

}
</script>
<style>
  .box-card {
    height: 300px;
    align-self: end;
    color: blue;
    background: magenta;
  }

  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .box-card {
    /* background: brown; */
    width: 480px;
  }
</style>
