<template>
  <div class="tile">
    <div class="tileSideBar"></div>
    <div class="tileGrid">
      <div class="tileTitle">
        {{ item.title }}
      </div>
      <div class="tileContent">
        <div class="tileMainContent">
          <div class="tileDescription">
            {{ item.description }}
          </div>
          <div class="tileFooter">
            <div class="tilePrice">
              <b>Price💰:</b> {{ item.price }} CalutulCoins
            </div>
            <div class="tileCommand">
              <b>Discord command:</b> <u>{{ item.command }}</u>
            </div>
          </div>
        </div>
        <div class="tilePlayContent">
          <div class="tileSoundDescription">
            Try the soundbite right here!⬇️
          </div>
          <audio :src="item.soundBiteUrl" controls></audio>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { constants } from '../common/constants'
export default {
  name: 'ShopTile',
  data: () => ({
    constants: constants
  }),
  props: ['item']
}
</script>

<style scoped>
.tile {
  display: grid;
  grid-template-columns: 2% 98%;
  width: 70%;
  margin: auto;
  height: 270px;
  background-color: #2f3136;
  border-radius: 15px 0 0 15px;
  font-family: 'Segoe UI';
  overflow: hidden;
  margin-bottom: 10px;
  color: white;
}

.tileGrid {
  display: grid;
  grid-template-rows: 25% 75%;
  border-left: solid 1px white;
}

.tileSideBar {
  display: block;
  width: 100%;
  background-color: #7289da;
}

.tileContent {
  display: grid;
  grid-template-columns: 65% 35%;
}

.tileMainContent {
  display: grid;
  grid-template-rows: 80% 20%;
  padding: 10px;
}

.tileFooter {
  display: grid;
  grid-template-columns: 45% 55%;
  padding-top: 10px;
}

.tileTitle {
  font-size: 50px;
  text-align: center;
  border-bottom: solid white 1px;
}

.tilePlayContent {
  display: grid;
  place-content: center;
  border-left: solid white 1px;
  overflow: hidden;
}

.tileSoundDescription {
  text-align: center;
  padding-bottom: 10px;
  font-size: 20px;
}

.tileDescription {
  font-family: Verdana;
  text-align: justify;
  background-color: rgba(255, 255, 255, 0.2);
  padding: 10px;
  border-radius: 10px;
  border: solid black 1px;
  box-shadow: 2px 2px black;
  box-shadow: black;
}

.tilePrice {
  font-size: 20px;
}

.tileCommand {
  text-align: right;
  font-size: 20px;
}
</style>
