<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
</template>

<script>
import { defineAsyncComponent } from 'vue'

// import HelloWorld from './components/HelloWorld.vue'

const AsyncComp = path => defineAsyncComponent(() =>
  import(`./components/${path}.vue`)
)

export default {
  name: 'App',
  components: {
    HelloWorld: AsyncComp('HelloWorld')
    // HelloWorld
  }
}
</script>
