<template>
  <MainPanel class="our-promise" :textPanelActive="true">
    <Title class="our-promise__title" :fontColor="'#5D62B5'">
      <template v-slot:title>
        Our promise to you
      </template>
      <template v-slot:subtitle>
        Sed perspiciatis omnis iste natus
      </template>
    </Title>
    <div class="our-promise__container">
      <Card 
      v-for="card in cards" 
      :key="card.id"
      :url="card.url"
      :title="card.title"
      :text="card.text"
      class="our-promise__card"
      :cardRow="true"
      />
    </div>
  </MainPanel>
</template>

<script>
import MainPanel from '@/components/MainPanel';
import Title from '@/components/Title';
import Card from '@/components/Card';
export default {
  components: {
    MainPanel,
    Title,
    Card,
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          url: 'https://i.ibb.co/7VQw9cs/dog-love.png',
          title: '24/7 Love & Care',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
        {
          id: 2,
          url: 'https://i.ibb.co/BKDHq0K/dog-vet.png',
          title: 'On-site Veterinarian',
          text: 'Dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt.'
        },
        {
          id: 3,
          url: 'https://i.ibb.co/52k7J2Y/dog-stream.png',
          title: 'Live-stream Cameras',
          text: 'Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur illum.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.our-promise__title {
  margin-bottom: 68px;
}
.our-promise__container {
  display: flex;
  justify-content: space-between;
}
@media screen and (max-width: 1024px) {
  .our-promise__container {
    flex-wrap: wrap;
  }
  .our-promise__card {
    margin-bottom: 50px;
  }
}
</style>