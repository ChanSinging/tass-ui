<!--
 * @Author: 申恒杰
 * @Date: 2023-02-09 12:24:45
 * @Description: 铁沸物
 * @FilePath: \tass-ui\docs\components\swiper\address.vue
-->
<template>
  <tass-carousel v-model="active3" indicator="outside">
    <tass-carousel-item id="1">
      <div style="color: white;text-align: center;width:100%;height:300px;line-height:300px;background-color:#009688;">条目一</div>
    </tass-carousel-item>
    <tass-carousel-item id="2">
      <div style="color: white;text-align: center;width:100%;height:300px;line-height:300px;background-color:#5FB878;">条目二</div>
    </tass-carousel-item>
    <tass-carousel-item id="3">
      <div style="color: white;text-align: center;width:100%;height:300px;line-height:300px;background-color:#FFB800;">条目三</div>
    </tass-carousel-item>
    <tass-carousel-item id="4">
      <div style="color: white;text-align: center;width:100%;height:300px;line-height:300px;background-color:#FF5722;">条目四</div>
    </tass-carousel-item>
  </tass-carousel>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {

    const active3 = ref("1")

    return {
      active3
    }
  }
}
</script>