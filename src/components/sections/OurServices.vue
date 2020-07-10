<template>
  <div>
    <Card 
    :url="cards[0].url"
    :title="cards[0].title"
    :text="cards[0].text"
    :cardColumn="true"
    />
  </div>
</template>

<script>
import Card from '@/components/Card';
export default {
  components: {
    Card,
  },
  data() {
    return {
      cards: [
        {
          id: '1',
          url: 'https://d.radikal.ru/d14/2006/78/c85556fd15a5.png',
          title: 'Pet Boarding (No Cages)',
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

</style>