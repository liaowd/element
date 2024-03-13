<template>
  <div style="margin: 20px;">
    <!-- filterable -->
    <!-- allow-create -->
    <el-select filterable allow-create select-single-input v-model="id" placeholder='请选择' @input="handleInput">
      <el-option v-for="item in list" :key="item.id" :label="item.name" :value="item.id" />
    </el-select>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        id: '',
        list: [ {
            id: '3',
            name: '司马sima',
          }]

      };
    },
    methods: {
      handleInput(val) {
        console.log(val);
      }
    }
  };
</script>
