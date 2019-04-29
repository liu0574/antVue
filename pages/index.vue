<template>
  <div class="outer">
    <div class="top">
      <section>测试运用后台</section>
    </div>
    <div class="left">
      <menu-left></menu-left>
    </div>
    <div class="content">
      <nuxt-child/>
    </div>
  </div>
</template>
<script>
import menuLeft from "~/components/MenuLeft.vue";
export default {
  components: {
    menuLeft
  },
  data() {
    return {
      labelCol: {
        xs: { span: 24 },
        sm: { span: 5 }
      },
      wrapperCol: {
        xs: { span: 24 },
        sm: { span: 12 }
      }
    };
  }
};
</script>
<style >
.outer {
  position: absolute;
  width: 100%;
  height: 95%;
  box-sizing: border-box;
}
.top {
  width: 100%;
  z-index: 1;
  position: fixed;
  height: 41px;
  background: rgb(84, 92, 100);
}
.top section {
  color: #ffffff;
  padding: 10px 20px;
}
.left {
  min-width: 200px;
  margin-top: 41px;
  height: 100%;
  width: 10%;
}
.content {
  top: 41px;
  /* margin-top: 50px; */
  width: 89%;
  position: absolute;
  margin-left: 210px;
}
</style>
