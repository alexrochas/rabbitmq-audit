<template>
  <div class="hello">
    <b-container fluid>
      <b-row>
        <b-col cols="6">
          <b-input-group prepend="uri">
            <b-form-input></b-form-input>
          </b-input-group>
        </b-col>
        <b-col cols="3">
          <b-input-group prepend="queue">
            <b-form-input></b-form-input>
          </b-input-group>
        </b-col>
        <b-col cols="1">
          <b-dropdown text="items" slot="append">
            <b-dropdown-item>10</b-dropdown-item>
            <b-dropdown-item>50</b-dropdown-item>
            <b-dropdown-item>100</b-dropdown-item>
            <b-dropdown-item>200</b-dropdown-item>
          </b-dropdown>
        </b-col>
        <b-col col="2">
          <b-button size="" v-on:click="search()" variant="primary">
            search
          </b-button>
        </b-col>
      </b-row>
      <b-row v-for="(value, index) in state.body" :key="index" >
        <Row :body=value></Row>
      </b-row>
    </b-container>
    <a href="#" class="float">
      <i class="fa fa-plus my-float"></i>
    </a>
  </div>
</template>

<script>
import Row from '@/components/Row';

export default {
  name: 'HelloWorld',
  components: {
    Row,
  },
  methods: {
    search() {
      this.state.body = ['B1', 'B2', 'B3'];
    },
  },
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      state: {
        body: [],
      },
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

  .float{
    position:fixed;
    width:60px;
    height:60px;
    bottom:40px;
    right:40px;
    background-color:#0C9;
    color:#FFF;
    border-radius:50px;
    text-align:center;
    box-shadow: 2px 2px 3px #999;
  }

  .my-float{
    margin-top:22px;
  }
</style>
