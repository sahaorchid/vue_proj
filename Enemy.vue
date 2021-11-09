<template>
  <div class="hello">
    <h1 @click="changeEmoji">{{emoji}}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorl',
  props:{
    emoji:String,
  },
  methods:{
      changeEmoji(){
          this.$emit("emojiChange","")
      }

  }
}
</script>


