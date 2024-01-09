<script>
export default {
  name: 'HelloWorld',

  data() {
    return {}
  },

  methods: {
    closeModal() {
      document.querySelector('#modal').remove();
    }
  }


}
</script>

<template>
  <div class="eb_overlay p-4 eb_film">
    <h1>Benvenuto nel mio sito</h1>

    <div class="eb_film" id="modal" @click="closeModal()">
      <div class="eb_modal border border-5">
        <h2>Questa è la modale che ti da il benvenuto</h2>
        <div class="eb_close-modal border border-1">X</div>
      </div>
    </div>
  </div>
</template>


<style lang="scss">
.eb_overlay {
  position: relative;
  text-align: center;
  margin: auto;

  .eb_film {
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 255, 255, 0.7);
    width: 100vw;
    height: 100vh;
  }

  .eb_modal {
    position: absolute;
    background-color: rgba(0, 0, 0, 0.8);
    top: 50%;
    right: 50%;
    transform: translate(50%, -50%);

  }

  .eb_close-modal {
    width: 2.5rem;
    aspect-ratio: 1 / 1;
    position: absolute;
    top: 0;
    right: 0;
    transform: translate(50%, -50%);
    font-size: 1.5rem;
    color: black;
    background-color: white;
    cursor: pointer;
    border-radius: 50%;
    transition: 0.5s;

    &:hover {
      border-color: black;
      background-color: black;
      color: white;
      transform: translate(50%, -50%) scale(1.2);
    }
  }

}
</style>