<template>
  <div class="about message">
    <div>
       Name: <input type="text" v-model="name" />
    </div>
  </div>
</template>
<script>
// @ is an alias to /src

export default {
  name: 'message',
  data () {
    return {
      name: ''
    }
  },
  watch: {
    'name': function () {
      this.callMe()
    }
  },
  methods: {
    // to update name value in parent component
    callMe () {
      this.$emit('name', this.name)
    }
  }
}
</script>
