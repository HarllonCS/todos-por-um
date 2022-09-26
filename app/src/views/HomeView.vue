<template>
  <div class="home">
  
    <Index/>
    
  </div>
</template>

<script>
// @ is an alias to /src
import Index from '@/components/index.vue'
import Tabelapais from '@/components/tabelapais.vue'

export default {
  name: 'HomeView',
  components: {
    Index,
    Tabelapais
  }
}
</script>
