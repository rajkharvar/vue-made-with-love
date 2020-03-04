<template>
  <div class="made-with-love">
    <p>
      {{ code ? '&lt;/&gt;' : 'Made' }} with ❤️
      {{ by ? 'by' : '' }}
      <span v-if="by" class="by">
        <a :href="link" v-if="link">{{ by }}</a>
        {{ !link ? by : '' }}
      </span>
    </p>
  </div>
</template>

<script>
export default {
  name: 'MadeWithLove',
  props: {
    by: {
      type: String,
      default: ''
    },
    link: {
      type: String,
      default: ''
    },
    code: {
      type: Boolean,
      default: false
    }
  }
}
</script>
