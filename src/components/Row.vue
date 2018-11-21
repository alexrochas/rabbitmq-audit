<template>
    <b-container fluid>
      <b-row>
        <b-col cols="10">
          {{ body }}
        </b-col>
        <b-col cols="2">
          <b-form-checkbox id="checkbox1"
                           value="accepted"
                           unchecked-value="not_accepted">
            ACK
          </b-form-checkbox>
        </b-col>
      </b-row>
    </b-container>
</template>

<script>
export default {
  name: 'Row',
  props: ['body'],
  data() {
    return {
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
