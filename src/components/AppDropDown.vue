<script>
export default {
    name: 'AppDropDown',
    data() {
        return {
          isOpen: false
        }
    },
    props: {
        dropdown: {
            type: Array,
            required: true,
        },
    },
  
  }

</script>

<template>
   <ul class="group-dropdown">
     <li v-for="item in dropdown" :key="item.label">
        <a :href="item.url">
            {{ item.label }}
        </a>
     </li>
  </ul>
</template>

<style lang="scss" scoped>

ul {
   margin-top: 30px;
   width: 200px ;
   background-color: $primary-color;  
   padding: 30px 30px;
   border-bottom: 2px solid $secondary-color;


    li {
      padding: 8px 0px;  

    a {
      text-decoration: none;
      color:$link-color;
      font-size: 14px;

      &:hover {
        color: $secondary-color;
      }
  }
}
}


</style>