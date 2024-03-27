<script setup>
import HomeIcon from "./Icons/Home.vue"
</script>
<template>
    <div id="LandingMenu">
        <h2>Select Options</h2>
        <div class="grids">
            <div class="options">
                <HomeIcon/>
                <h4>Menu1</h4>
            </div>
            <div class="options">
                <HomeIcon/>
                <h4>Menu2</h4>
            </div>
            <div class="options">
                <HomeIcon/>
                <h4>Menu3</h4>
            </div>
            <div class="options">
                <HomeIcon/>
                <h4>Menu4</h4>
            </div>
        </div>
    </div>
</template>

<style scoped>

#LandingMenu{
    max-width: 300px;
}

.grids{
    display: grid;
    gap: 15px;
    grid-template: repeat(2,1fr)/repeat(2,1fr);
}
.options{
    display: grid;
    padding: 10px 15px;
    border-radius: 4px;
    background-color: rgb(32, 32, 32);
    cursor: pointer;
    align-items: center;
    min-width: 200px;  
    grid-template-columns: 40px auto;
    grid-column-gap: .5em;
}
.icon{
    max-width: 30px;
    background-color: var(--bg-light-green);
    border-radius: 5px;
    padding: 0.25em;
    display: inline-flex;
    place-self: center;
;
}
svg{
    width: 100%;
}
</style>