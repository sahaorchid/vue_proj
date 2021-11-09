<template>
  <div class="hello">
    <progress  :value="value" max="100"> 32% </progress>
    
    
    <Enemy v-if="value>70 && value<=100" @emojiChange="valueChange" emoji="👿"/>
    <Enemy v-else-if="value>40 && value<=70" @emojiChange="valueChange" emoji="😭"/>
    <Enemy v-else-if="value>10 && value<=40" @emojiChange="valueChange" emoji="🤕"/>
    <Enemy v-else @emojiChange="valueChange" emoji="😵"/>

  </div>
</template>

<script>
import Enemy from "./Enemy"
export default {
  name: 'HelloWorl',
  components: {
    Enemy
  },
  data(){
    return {
      value:100

    }
  },
  methods:{
    valueChange(){
      this.value-=10
    },


  }
}
</script>


