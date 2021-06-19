<template>
 <div>
    <component 
     :is="type" 
     :to="to"
     :href="href"
     :modal="modal"
     :submit="submit"
     :reset="reset"
  >
    <slot/>
  </component>
 </div>
</template>

<script>
  export default {
    props: {
      href: {
        type: String,
        default: null
      },
      to: {
        type: String,
        default: '/'
      },
      modal:{
        type:Boolean,
        default:false
      },
      submit:{
        type:String,
        default:null
      },
      reset:{
        type:String,
        default:null
      }
    },
    computed: {
      type() {
        if (this.href) {
          return 'a'
        }
        else if(this.to){
          return 'n-link'
        }
        else if(this.submit){
          return 'button'
        }
        else if(this.reset){
          return 'button'
        }
        else if(this.modal){
          return 'v-b-modal.my-modal'
        }
         else {
          return 'button'
        }
      }
     
    }
  }
</script>

<style scoped>
 
</style>