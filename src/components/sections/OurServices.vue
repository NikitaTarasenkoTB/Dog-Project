<template>
<div class="page">
  <MainPanel class="services" :textPanelActive="true">
    <Title class="services__title" :fontColor="'#5D62B5'">
      <template v-slot:title>
        Our services
      </template>
      <template v-slot:subtitle>
        Sed perspiciatis omnis iste natus
      </template>
    </Title>
    <div class="grid-container">
      <Card 
      v-for="card in cards" :key="card.id"
      :url="card.url"
      :title="card.title"
      :text="card.text"
      :cardColumn="true"
      />
    </div>
    <Button class="services__button">learn more</Button>
  </MainPanel>
</div>
</template>

<script>
import Card from '@/components/Card';
import MainPanel from '@/components/MainPanel';
import Title from '@/components/Title';
import Button from '@/components/ui/Button';
export default {
  components: {
    Card,
    MainPanel,
    Title,
    Button,
  },
  data() {
    return {
      cards: [
        {
          id: '1',
          url: 'https://d.radikal.ru/d14/2006/78/c85556fd15a5.png',
          title: 'Pet Boarding',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
        {
          id: '2',
          url: 'https://b.radikal.ru/b12/2006/19/39d88ab89a84.png',
          title: 'Pet Daycare',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
        {
          id: '3',
          url: 'https://c.radikal.ru/c39/2006/08/075220591d8d.png',
          title: 'Pet Day Spa & Grooming',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
        {
          id: '4',
          url: 'https://b.radikal.ru/b14/2006/fe/144a8b9421c0.png',
          title: 'Custom Meal Plans',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
        {
          id: '5',
          url: 'https://c.radikal.ru/c13/2006/11/137c1b0c4c19.png',
          title: 'Pet Training',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
        {
          id: '6',
          url: 'https://d.radikal.ru/d23/2006/ee/b7b1870febfc.png',
          title: 'Shop Our Store!',
          text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium corrupti quos dolores et quas.'
        },
      ]
    }
  }
}
</script>

<style scoped>
.page {
  background-color: #F5F5F5;
  color: black;
  position: relative;
  z-index: 0;
}
.page::before {
  content: "";
  display: block;
  position: absolute;
  top: 0;
  right: 0;
  background-image: url('../../assets/images/blob2.png');
  background-repeat: no-repeat;
  background-position: top right;
  width: 100%;
  height: 100%;
  z-index: -1;
}
.services {
  margin: 0 auto;
  padding-top: 100px;
  padding-bottom: 112px;
  z-index: 2;
}
.services__title {
  margin-bottom: 78px;
}
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  grid-gap: 24px;
  align-items: center;
  justify-items: center;
  margin-bottom: 66px;
}
.services__button {
  margin: 0 auto;
  display: flex;
  justify-content: center;
}
</style>