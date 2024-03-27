<script setup>
import Sidebar from './components/Sidebar.vue'
import LandingMenu from "./components/Landing.vue";
import Home from './components/Icons/Home.vue';
</script>
<template>
  <div class="wrapper">
    <div id="Sidebar">
      <button>
        <Home/>
      </button>
      <button>
        <Home/>
      </button>
      <button>
        <Home/>
      </button>
      <button>
        <Home/>
      </button>
      <button>
        <Home/>
      </button>
      <button>
        <Home/>
      </button>

    </div>
    <div id="ContentList">
      <h2>Notes</h2>
      <div class="header">
        <form class="input-wrapper icon-inline" @submit.prevent="console.log('search')">
          <input type="text" placeholder="search">
          <button>
            <Home/>
          </button>
        </form>
      </div>
      <div class="list vertical-grid">
        <div class="items">
          <h3>Main Title</h3>
          <h4>Sub Title</h4>
          <p>Conetnt Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus perferendis recusandae tempora. Necessitatibus ut labore, ratione deserunt, sapiente porro, possimus veritatis quaerat magnam obcaecati eius doloribus hic quia! Aliquid, mollitia.</p>
        </div>
        <div class="items">aasd</div>
        <div class="items">sada</div>
        <div class="items">asdas</div>
        <div class="items">asdas</div>
        <div class="items">sdfsdf</div>
      </div>
    </div>
    <div id="main">

    </div>
  </div>
</template>

<style scoped>
.wrapper{
  font-size: 1.4rem;
  min-height: 100vh;
  padding: 1em;
  overflow: hidden;
  display: grid;
  grid-template-columns: 70px 320px auto;
}
#Sidebar{
  max-width: 70px;
  border-right: 1px solid var(--dark-border);
  padding: 1rem;
  background-color: var(--bg-sidebar);
  border-radius: 4px;
  display: grid;
  grid-auto-rows: min-content;
  grid-row-gap: 1em;
}
#ContentList{
  padding: 1rem;
  border-inline-end: 1px solid var(--dark-border);
}
</style>

<style lang="scss">
#Sidebar{
  button{
    padding: 1rem;
  }
}
#ContentList h2{
  margin-top: 0;
}
#ContentList{
  & > * {
    margin-block: 1rem;
  }
  .items {
    border-radius: 4px;
    background-color: var(--bg-dark);
    h3, h4 ,p{
      margin: 0;
    }
    max-height: 150px;
    // border: 1px solid var(--grey-border);
    padding: 1rem;
    overflow: hidden;
    white-space: nowrap;
  }
  p{
    max-width: 99%;
    overflow: hidden;
    text-overflow: ellipsis;
  }
}
.input-wrapper{
  border: 1px solid var(--dark-border);
  border-radius: 4px;
  letter-spacing: -0.45px;
}
.icon-inline{
  display: grid;
  grid-template-columns: auto 2rem;
  gap: 1rem;
  padding-inline: .5rem;
}
input{
  padding: .5rem .75rem;
  border:none;
  outline: none;
  font-size: 1.4rem;
  height: 5rem;
  background-color: transparent;
  & + button{
    max-width: 3rem;
    padding: 0;
    background-color: transparent;
    outline: none;
    border: none;
  }
}
</style>