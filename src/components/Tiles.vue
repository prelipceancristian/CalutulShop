<template>
  <div class="pt-5">
    <div v-for="item in items" :key="item.command">
      <ShopTile :item="item"> </ShopTile>
    </div>
  </div>
</template>

<script>
import ShopTile from './ShopTile.vue'

export default {
  name: 'HelloWorld',
  components: {
    ShopTile
  },

  data: () => ({
    items: [
      {
        title: 'Title1',
        description: 'this is the item description. should be a few lines long',
        price: 1500,
        command: '!buy 100',
        imageURL: '',
        soundBiteUrl: ''
      },
      {
        title: 'Title2',
        description: 'this is the item description. should be a few lines long',
        price: 2500,
        command: '!buy 200',
        imageURL: '',
        soundBiteUrl: ''
      },
      {
        title: 'Title3',
        description: 'this is the item description. should be a few lines long',
        price: 2500,
        command: '!buy 300',
        imageURL: '',
        soundBiteUrl: ''
      }
    ]
  })
}
</script>
