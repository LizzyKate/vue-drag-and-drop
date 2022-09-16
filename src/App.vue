<template>
<div id="app">
  <main class="flexbox">
    <TemplateBoard :id="'board-1'">
      <TemplateCard :id="'card-1'" :draggable="true">
        <p>Card 1</p>
      </TemplateCard>
    </TemplateBoard>
    <TemplateBoard :id="'board-2'">
      <TemplateCard :id="'card-2'" :draggable="true">
        <p>Card 2</p>
      </TemplateCard>
    </TemplateBoard>
  </main>
</div>
</template>

<script>
import TemplateCard from './components/TemplateCard.vue'
import TemplateBoard from './components/TemplateBoard.vue'

export default {
  name: 'App',
  components: {
    TemplateCard,
    TemplateBoard,

}
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body{
  font-family: 'Poppins', sans-serif;
  background: #f5f5f5;
}
.flexbox{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 768px;
  height: 100vh;
  overflow: hidden;
  margin: 0 auto;
  padding: 15px;
}
.flexbox .board{
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 400px;
  background: #313131;
  padding: 15px;
  height: 90vh;
  margin-right: 8px;
}
.flexbox .board .card{
  padding: 15px;
  background: #f3f3f3;
  cursor: pointer;
  margin-bottom: 15px;
}
</style>
