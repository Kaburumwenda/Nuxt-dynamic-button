<template>
  <div id="app">
    <b-button
      type="button"
      class="btn"
      variant="info"
      @click="showModal"
    >
      Open About Modal
    </b-button>

    <Bs-modal
      v-show="isModalVisible"
      @close="closeModal"
    >

    <template #body>
        <h1>About modal content</h1>
        <p>model</p>
    </template>

      <template #footer>
        <h1>About modal content</h1>
    </template>

    </Bs-modal>
   
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