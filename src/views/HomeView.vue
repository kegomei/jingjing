<template>
  <div class="home">
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Options({
  components: {
    HelloWorld,
  },
  data: () => {
    return {
      cao: 23
    }
  }
})
export default class HomeView extends Vue {
  cao!: string;
}
</script>
