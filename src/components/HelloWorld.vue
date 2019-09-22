<template>
  <div class="hello bg-info">
    <Menu></Menu>
    <Menu2></Menu2>
    <Animes></Animes>
    <W3Card></W3Card>
    
    <W3Card1></W3Card1>
    <h1>{{ msg }}</h1>
    <Button1></Button1>
    <InputPare></InputPare>
    <p>fs4</p>
    <Input1></Input1>
    <RowCard></RowCard>
    <ColCard></ColCard>
    <ImageWithLoad></ImageWithLoad>
    <CardContainer></CardContainer>
    
    <CardContainer1></CardContainer1>
    <CardFlex></CardFlex>
    <MoveForwadImage :imgHeight=50 ></MoveForwadImage>
    <FixedImage :imgHeight=50  ></FixedImage>
    <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel"
          target="_blank"
          rel="noopener"
          >babel</a
        >
      </li>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint"
          target="_blank"
          rel="noopener"
          >eslint</a
        >
      </li>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-unit-jest"
          target="_blank"
          rel="noopener"
          >unit-jest</a
        >
      </li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li>
        <a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a>
      </li>
      <li>
        <a href="https://forum.vuejs.org" target="_blank" rel="noopener"
          >Forum</a
        >
      </li>
      <li>
        <a href="https://chat.vuejs.org" target="_blank" rel="noopener"
          >Community Chat</a
        >
      </li>
      <li>
        <a href="https://twitter.com/vuejs" target="_blank" rel="noopener"
          >Twitter</a
        >
      </li>
      <li>
        <a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a>
      </li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li>
        <a href="https://router.vuejs.org" target="_blank" rel="noopener"
          >vue-router</a
        >
      </li>
      <li>
        <a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/vue-devtools#vue-devtools"
          target="_blank"
          rel="noopener"
          >vue-devtools</a
        >
      </li>
      <li>
        <a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener"
          >vue-loader</a
        >
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
          rel="noopener"
          >awesome-vue</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
import Button1 from "./Buttons/Button";
import Input1 from "./Inputs/Input";
import MoveForwadImage from "./Images/MoveForwadImage";
import FixedImage from './Images/FixedImage'
import ImageWithLoad from './Images/ImageWithLoad'
import RowCard from "./Cards/RowCard";
import ColCard from "./Cards/ColCard";
import InputPare from "./Inputs/InputPare";
import CardContainer from "./Containers/CardContainer";
import CardContainer1 from "./Containers/CardContainer1";
import CardFlex from "./Containers/CardFlex";
import Fonts from "./Fonts/ResponsiveFont";

import Menu from "./Menus/menu";
import Menu2 from "./Menus/Menu2";
import W3Card from "./W3Component/Card";

import W3Card1 from "./W3Component/Card-1";
import Animes from "./Animation/AnimationTest";
export default {
  name: "HelloWorld",
  components:{
    Button1,Input1,MoveForwadImage,FixedImage
    ,RowCard,ColCard,InputPare,ImageWithLoad,
    CardContainer,CardFlex,CardContainer1,Fonts,
    Menu,W3Card,W3Card1,Menu2,Animes
  },
  mounted(){
    window.addEventListener("resize",this.helloResize)
  },
  beforeDestroy(){
    window.removeEventListener("resize",this.helloResize)
  },
  methods:{
    helloResize(){
      console.log('this hello resize')
    }
  },
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
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
