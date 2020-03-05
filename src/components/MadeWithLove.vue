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

<style lang="scss" scoped>
.made-with-love {
  text-align: center;
  background: transparent;
  font-family: Avenir, Helvetica, Arial, sans-serif;

  p {
    position: absolute;
    bottom: 0;
    width: 100%;
    left: 0;
  }

  .by {
    font-weight: bold;

    a {
      text-decoration: none;
      color: inherit;

      &:hover {
        border-bottom: 1px solid;
      }
    }
  }
}
</style>
