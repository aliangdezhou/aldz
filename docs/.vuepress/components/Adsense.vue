<template>
  <script
    v-if="show"
    :data-ad-client="dataAdClient"
    src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"
    async="true"
  ></script>
</template>

<script>
export default {
  props: {
    dataAdClient: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      show: process.env.NODE_ENV === 'production'
    }
  }
}
</script>
