<template>
  <div class="greetings">
    <h1 @[eventName]="onClick" class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<script>
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'HelloWorld',
    props: {
      msg: {
        type: String,
        required: true
      }
    },
    computed: {
      eventName() {
        return 'click';
      }
    },
    methods: {
      onClick() {
        console.log('Clicked h1');
      }
    }
  });
</script>

<style scoped>
  h1 {
    font-weight: 500;
    font-size: 2.6rem;
    top: -10px;
  }

  h3 {
    font-size: 1.2rem;
  }

  .greetings h1,
  .greetings h3 {
    text-align: center;
  }

  @media (min-width: 1024px) {
    .greetings h1,
    .greetings h3 {
      text-align: left;
    }
  }
</style>
