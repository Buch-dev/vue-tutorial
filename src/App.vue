<template>
  <!-- <BindingsComponent /> -->
  <!-- <ConditionalRendering /> -->
  <!-- <ListRendering /> -->
  <!-- <ConditionalListRendering /> -->
  <!-- <MethodsComponent /> -->
  <!-- <EventHandling /> -->
  <!-- <FormHandling /> -->
  <!-- <BonusDirective /> -->
  <!-- <ComputedProperties /> -->
  <!-- <WatchersComponent /> -->
  <!-- <Greet name="Bruce" heroName="Batman" />
  <Greet name="Clark" heroName="Superman" />
  <Greet name="Diana" heroName="Wonder Woman" />
  <Greet :name="name" :heroName="channel" /> -->

  <!-- <Article id="my-article" title="Article Title" :likes="50" :isPublished="true" /> -->
  <!-- Provide/Inject -->
  <!-- <h3>AppComponent username {{ name }}</h3>
  <ComponentC /> -->
  <!-- Component Events -->
  <!-- <button @click="showPopup = true">Show Popup</button> -->
  <!-- <Popup v-show="showPopup" @close="closePopup" /> -->

  <!-- Components and v-model -->
  <!-- <input type="text"> -->
  <!-- <InputComponent v-model="name" /> -->

  <!-- Slot -->
  <!-- <Card></Card>
  <Card>Card content</Card>
  <Card>
    <h2>Card content</h2>
  </Card>
  <Card>
    <img src="https://picsum.photos/200" />
  </Card> -->
  <!-- Named Slot -->
  <!-- <Card>
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img src="https://picsum.photos/200" />
    </template>
    <template v-slot:footer><button>View details</button></template>
  </Card> -->

  <!-- Slots Props -->
  <!-- <NamedList>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} {{ slotProps.lastName }}
    </template>
  </NamedList>
  <NamedList>
    <template v-slot:default="slotProps">
      {{ slotProps.lastName }} {{ slotProps.firstName }}
    </template>
  </NamedList>
  <NamedList>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }}
    </template>
  </NamedList> -->

  <!-- Component Styles -->
  <!-- <h4>App component text</h4>
  <ChildStyles>
    <h4>Childstyles component text</h4>
  </ChildStyles> -->

  <!-- Dynamic Components -->
  <!-- <button @click="activeTab = 'TabA'">Tab A</button>
  <button @click="activeTab = 'TabB'">Tab B</button>
  <button @click="activeTab = 'TabC'">Tab C</button>

  <keep-alive>
    <component :is="activeTab" />
  </keep-alive> -->

  <!-- <TabA v-if="activeTab === 'TabA'" />
  <TabB v-if="activeTab === 'TabB'" />
  <TabC v-if="activeTab === 'TabC'" /> -->

  <!-- Teleport Component -->
  <!-- <teleport to='#portal-root'>
    <Portal />
  </teleport> -->

  <!-- HTTP GET Request -->
  <!-- <PostList /> -->

  <!-- HTTP POST Request -->
  <!-- <CreatePost /> -->

  <!-- Lifecycle Hooks -->
  <!-- <Parent /> -->

  <!-- Template Refs -->
  <!-- <TemplateRef /> -->

  <!-- Reusability with Mixins and Composables -->
  <ClickCounter />
  <HoverCounter />

  <!-- Composition API -->
  <!-- <Data /> -->

  <!-- Reactivity and toRefs -->
  <!-- <Demo /> -->
  <!-- <DemoTwo /> -->

  <!-- Replacing Methods -->
  <!-- <MethodsComposition /> -->

  <!-- v-model and composition API -->
  <!-- <VModel /> -->

  <!-- Computation and composition API -->
  <!-- <Computed /> -->

  <!-- Replacing Watchers (Part 1) -->
  <!-- <Watch /> -->

  <!-- Replacing Provide/Inject -->
  <!-- <ProvideInject /> -->

  <!-- Template Refs and Composition -->
  <!-- <TemplateRefC /> -->

  <!-- Props and Composition API -->
  <!-- <Person /> -->
</template>

<script>
// import BindingsComponent from './components/Bindings.vue'
// import ConditionalRendering from './components/ConditionalRendering.vue'
// import ListRendering from './components/ListRendering.vue'
// import ConditionalListRendering from './components/ConditionalListRendering.vue'
// import MethodsComponent from './components/MethodsComponent.vue'
// import EventHandling from './components/EventHandling.vue'
// import FormHandling from './components/FormHanding.vue'
// import BonusDirective from './components/BonusDirective.vue'
// import ComputedProperties from './components/ComputedProperties.vue'
// import WatchersComponent from './components/WatchersComponent.vue'
// -------------Components-------------
// import Greet from "./components/Greet.vue";
// import Article from "./components/Article.vue";
// import ComponentC from "./components/ComponentC.vue";
// import Popup from './components/Popup.vue'
// import InputComponent from './components/Input.vue'
// import Card from "./components/Card.vue";
// import NamedList from "./components/NamedList.vue";
// import ChildStyles from './components/ChildStyles.vue'
// import TabA from "./components/TabA.vue";
// import TabB from "./components/TabB.vue";
// import TabC from "./components/TabC.vue";
// import Portal from './components/Portal.vue'
// import PostList from './components/PostList.vue'
// import CreatePost from './components/CreatePost.vue'
// import Parent from './components/Parent.vue'
// import TemplateRef from './components/TemplateRef.vue'
import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'
// import Data from './components/Data.vue'
// import Demo from './components/DemoOne.vue'
// import DemoTwo from './components/DemoTwo.vue'
// import MethodsComposition from './components/Methods.vue'
// import VModel from './components/VModel.vue'
// import Computed from './components/Computed.vue'
// import Watch from './components/Watch.vue'
// import ProvideInject from './components/ProvideInject.vue'
// import TemplateRefC from './components/TemplateRefC.vue'
// import Person from './components/Person.vue'

export default {
  name: "App",
  components: {
    // BindingsComponent,
    // ConditionalRendering,
    // ListRendering
    // ConditionalListRendering
    // MethodsComponent
    // EventHandling
    // FormHandling
    // BonusDirective
    // ComputedProperties
    // WatchersComponent
    // Greet,
    // Article,
    // ComponentC,
    // Popup
    // InputComponent
    // Card,
    // NamedList,
    // ChildStyles
    // TabA,
    // TabB,
    // TabC,
    // Portal
    // PostList,
    // CreatePost
    // Parent
    // TemplateRef
    ClickCounter,
    HoverCounter
    // Data
    // Demo
    // DemoTwo
    // MethodsComposition
    // VModel
    // Computed
    // Watch
    // ProvideInject
    // TemplateRefC
    // Person
  },
  data() {
    return {
      // name: "Buchman",
      channel: "Buchcodx",
      showPopup: false,

      // Components and v-model
      name: "",

      // Dynamic Components
      activeTab: "TabA",
    };
  },
  methods: {
    closePopup(name) {
      this.showPopup = false;
      console.log("name", name);
    },
  },
  provide() {
    return {
      username: this.name,
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

h4 {
  color: orange;
}
</style>
