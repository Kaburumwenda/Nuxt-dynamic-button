<template>
   <div>
       <h1>Reusable Button</h1>

       <sb-button>
           <b-button 
           v-if="permissions==1"
           :variant="theme" 
           :size="size"
           :block="block"
           :active ="isactive"
           :pill="pill"
           :squared ="squared"
           >
            {{text}}
           </b-button>
           <b-button v-else :disabled="disabled" :block="block"> {{text}}</b-button>
       </sb-button>

   </div>
</template>

<script>
export default {
   data(){
       return{
           permissions:1
       }
   },

   methods:{
       getUser(){
       }
   },

   props: {
       href: {
        type: String,
        default: '/'
      },
      to: {
        type: String,
        default: null,
      },
      modal:{
        type:Boolean,
        default:null
      },
      size:{
          type:String,
          default:null
      },
      block:{
          type:Boolean,
          default:true
      },
      isactive:{
          type:Boolean,
          default:false
      },
      pill:{
          type:Boolean,
          default:false
      },
      squared:{
          type:Boolean,
          default:false
      },
      disabled:{
          type:Boolean,
          default:false
      },
      theme:{
          type:String,
          default:'success'
      },

      icon:{
          type:String,
          default:null
      },
      text:{
          type:String,
          default:"click me"
      }
    },
  
}
</script>

<style scoped>

</style>