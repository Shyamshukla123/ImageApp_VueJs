<script setup>
    import {defineEmits} from 'vue';

    const emits =defineEmits(["selectOption"]);
    const OpctionSelected=(isColored)=>{
        emits("selectOption",isColored);
    }
</script>


<template>
  <v-navigation-drawer
        expand-on-hover
        rail
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Shyam shukla"
            subtitle="shyamshukla789@gmail.com"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item 
          prepend-icon="mdi-image" 
          title="shyam gallery" 
          value="Gallery"
          @click="OpctionSelected(true)"
          >
        </v-list-item>
          <v-list-item 
          prepend-icon="mdi-star" 
          title="change color" 
          value="starred"
          @click="OpctionSelected(false)"
          >
        </v-list-item>
        </v-list>
      </v-navigation-drawer>
      
</template>



