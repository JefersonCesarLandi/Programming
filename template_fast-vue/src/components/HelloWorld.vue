<template>
  <fast-design-system-provider use-defaults>
    <fast-card>
      <h2>{{msg}}</h2>
      <fast-button appearance="accent" v-on:click="onClick">Click Me</fast-button>
    </fast-card>
  </fast-design-system-provider>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    onClick: function () {
      console.log('clicked!');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  fast-design-system-provider {
    display: block;
  }

  fast-card {
    padding: 16px;
    display: flex;
    flex-direction: column;
  }

  h2 {
    font-size: var(--type-ramp-plus-5-font-size);
    line-height: var(--type-ramp-plus-5-line-height);
  }

  fast-card > fast-button {
    align-self: flex-end;
  }
</style>
