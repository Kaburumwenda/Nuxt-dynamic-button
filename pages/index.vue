
<template>
  <div id="app">
    <b-button
      type="button"
      class="btn"
      @click="showModal"
    >
      Default Modal
    </b-button>

    <Bs-modal
      v-show="isModalVisible"
      @close="closeModal"
    ></Bs-modal>
   
  </div>
</template>


<script>
  export default {
    components: {
      
    },
    data () {
      return {
        isModalVisible: false,
      };
    },
    methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    },
  };
</script>