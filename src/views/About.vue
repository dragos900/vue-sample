<template>
  <div class="about">
    <h1>This is an about page. You can check parent-child binding</h1>
    <Message @name="getName" />
    <br/><br/>
    <u>Message from Child</u>: {{name}}
  </div>
</template>
<script>
import Message from '@/components/Message.vue'
export default {
  name: 'about',
  components: {
    Message
  },
  data () {
    return {
      name: ''
    }
  },
  methods: {
    // Recieve value from child
    getName (val) {
      //    set name value
      this.name = val
    }
  }
}
</script>
