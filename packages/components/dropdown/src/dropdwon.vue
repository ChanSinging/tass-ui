<!--
    * @Name: dropdwon
    * @Author: cxy
    * @Date: 2023/2/1 17:55
    * @Description：dropdwon
    * @Update: 2023/2/1 17:55
-->
<template>
    <div class="tass-dropdown"
         @mouseenter="mouseenter"
         @mouseleave="mouseleave">
        <button class="dropdown-button" @click="mouseclick">
            <span class="tass-dropdown-link" >
                下拉菜单
                <tass-icon style="margin-left: 10px" name="chevrondown"></tass-icon>
            </span>
        </button>
        <slot></slot>
    </div>

</template>

<script setup lang="ts">
  import '../style/'
  import mitt from "./event";

  const props = defineProps({
    trigger: {
        type: [String],
        default: 'hover'
    }
  })
  const mouseclick = () => {
    if(props.trigger === 'click'){
        mitt.emit('updateShowMenuClick', true)
    }
  };
  const mouseenter = () => {
      if(props.trigger === 'hover'){
          mitt.emit('updateShowMenu', true)
      }
  }
  const mouseleave = () => {
      mitt.emit('mouseleave', false)
  }

</script>

