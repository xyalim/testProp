<template>
  <view>
    <!-- 1.我无法直接在模板里直接使用 typeof 但h5可以 -->
    <!-- 2. 
      Function类型的default值
      H5 function  小程序 string
    -->
    defaultFuncType prop type: {{ defaultFuncType }}
    propFunc prop type: {{ propFuncType }}
  </view>
</template>

<script>
  export default {
    name: 'TestFunctionProp',
    props: {
      defaultFunc: {
        type: Function,
        default(){
          return 'this is string'
        }
      },
      propFunc: {
        type: Function,
        default(){
          return 'this is propFunc'
        }
      },
    },
    computed:{
      defaultFuncType(){
        return typeof this.defaultFunc
      },
      propFuncType(){
        return typeof this.propFunc
      },
    },
    methods: {

    },
  }
</script>

<style lang="scss" scoped>

</style>