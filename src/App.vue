<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <MyComponent msg="App-test" />
    <!-- <TemplateSyntax msg="TemplatessSyntax"/> -->
    <Counter />
    <br />
    <Props />
    <br />
    <Computed />
    <br />
    <Methods />
    <br />
    <WatchedProperty />
    <br />
    <BindingHtmlClasses />
    <br />
    <ConditionalRendering />
    <br />
    <ListRendering />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MyComponent from "./components/MyComponent.vue";
// import TemplateSyntax from './components/TemplateSyntax.vue'
import Counter from "./components/Counter.vue";
import Props from "./components/Props.vue";
import Computed from "./components/Computed.vue";
import Methods from "./components/Methods.vue";
import WatchedProperty from "./components/WatchedProperty.vue";
import BindingHtmlClasses from "./components/BindingHtmlClasses.vue";
import ConditionalRendering from "./components/ConditionalRendering.vue";
import ListRendering from "./components/ListRendering.vue";


export default {
  name: "App",
  components: {
    // HelloWorld,
    MyComponent,
    // TemplateSyntax,
    Counter,
    Props,
    Computed,
    Methods,
    WatchedProperty,
    BindingHtmlClasses,
    ConditionalRendering,
    ListRendering,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
