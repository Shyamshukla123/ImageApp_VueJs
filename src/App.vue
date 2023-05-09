<script setup>

import ImageGallery from './components/ImageGallery.vue';
import SideBar from './components/SideBar.vue';
import {ref} from 'vue'

const isWithColor= ref(true);

const onSelectOption=(isColor)=>{
  isWithColor.value=isColor;
}

</script>


<template>
  <VApp>
   
      <!-- SIDE BAR -->
      <SideBar @selectOption="onSelectOption"/>
      <VMain>
          <!-- Cards  -->
          <ImageGallery :isWithColor="isWithColor"/>
      </VMain>
  </VApp>
</template>

