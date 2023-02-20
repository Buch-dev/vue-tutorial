<template>
    <img alt="Vue logo" src="../assets/logo.png" />
    <div>{{ greet }} {{ name }}</div>
    <div v-html="channel"></div>
    <div v-html="hack"></div>
    <h2 :id="headingId">Heading</h2>
    <button :disabled="isDisabled">Bind</button>
    <h2 class="underline">Underlined text</h2>
    <h2 class="underline" :class="status">Status</h2>
    <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
    <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout? movie</h2>
    <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>
    <h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">
      Array Conditional Movie
    </h2>
    <h2
      :class="{
        promoted: isPromoted,
        new: !isSoldout,
        'sold-out': isSoldout,
      }"
    >
      Object Conditional Movie
    </h2>
    <h2
      :style="{
        color: highlightColor,
        fontSize: headerSize,
        padding: '20px',
      }"
    >
      Inline Style
    </h2>
    <h2 :style="headerStyleObject">Style Object</h2>
  
    <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
    <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
  </template>
  
  <script>
  export default {
    name: "BindingsComponent",
    data() {
      return {
        greet: "Hello",
        name: "Buchman",
        channel: "<b>Codeevolution</b>",
        hack: '<a href="#" onclick="alert("You have been hacked!")">Win a prize!</a>',
        headingId: "heading",
        isDisabled: true,
        status: "danger",
        isPromoted: false,
        isSoldout: false,
        highlightColor: "orange",
        headerSize: "50px",
        headerStyleObject: {
          color: "orange",
          fontSize: "50px",
          padding: "20px",
        },
        baseStyleObject: {
          fontSize: "50px",
          padding: "10px",
        },
        successStyleObject: {
          color: "green",
          backgroundColor: "lightgreen",
          border: "1px solid green",
          padding: "20px",
        },
        dangerStyleObject: {
          color: "darkred",
          backgroundColor: "red",
          border: "1px solid darkred",
        },
      };
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
  
  .underline {
    text-decoration: underline;
  }
  
  .promoted {
    font-style: italic;
  }
  
  .new {
    color: olivedrab;
  }
  
  .sold-out {
    color: red;
  }
  </style>
  