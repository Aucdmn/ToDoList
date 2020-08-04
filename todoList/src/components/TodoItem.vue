<template>
    <div>
        <li class="item" @click="handleDelete">{{content}}</li>
    </div>
</template>

<script>
export default {
  props: ['content', 'index'],
  methods: {
    handleDelete () {
      this.$emit('delete', this.index)
    }
  }
}
</script>

// 使用scoped：添加局部样式；不加上scoped：全局样式
<style scoped>
  .item{
    color: aquamarine;
  }
</style>
