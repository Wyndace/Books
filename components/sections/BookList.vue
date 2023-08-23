<template>
  <WynSection>
    <WynContent class="flex flex-col gap-9">
    <div class="flex justify-between items-center gap-1">
      <WynBadge class="bg-red-400">{{ title }}</WynBadge>
      <div class="flex gap-2">
      </div>
    </div>
      <ul class=" flex items-center justify-between gap-1">
        <li v-for="book in Books" :key="book.id" class="w-[185px]">
          <WynBookCard :book="book" />
        </li>
      </ul>
    </WynContent>
  </WynSection>
</template>


<script setup lang="ts">
  import WynSection from "~/components/UI/WynSection.vue"
  import WynContent from "~/components/UI/WynContent.vue"
  import WynBadge from '~/components/UI/WynBadge.vue';
  import WynBookCard from "~/components/UI/WynBookCard.vue"
  defineProps({
    title: String,
    filter: String,
  })
  const Books = [
    {
      price: {
          old_value: 2099,
          value: 1099,
          currency: '₽'
        },
      about: {
        title: 'Сверхъестественное. Подлинная история братьев',
        link: '/books/1',
        img: '/sources/books/Supernatural.png'
      },
      author: {
        full_name: "Елизавета Бута",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 4,
      reviews: 41,
      id: 1,
    },
    {
      price: {
          value: 0,
          currency: '₽'
        },
      about: {
        title: 'Тайна жожеков с красной планеты',
        link: '/books/2',
        img: '/sources/books/placholder.png'
      },
      author: {
        full_name: "Социал-шаурмист",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 5,
      reviews: 99999999,
      id: 2,
    },
    {
      price: {
          old_value: 2099,
          value: 1099,
          currency: '₽'
        },
      about: {
        title: 'Сверхъестественное. Подлинная история братьев',
        link: '/books/3',
        img: '/sources/books/Supernatural.png'
      },
      author: {
        full_name: "Елизавета Бута",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 2.3,
      reviews: 41,
      id: 3,
    },
    {
      price: {
          value: 0,
          currency: '₽'
        },
      about: {
        title: 'Тайна жожеков с красной планеты',
        link: '/books/4',
        img: '/sources/books/placholder.png'
      },
      author: {
        full_name: "Социал-шаурмист",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 5,
      reviews: 99999999,
      id: 4,
    },
    {
      price: {
          old_value: 209099999,
          value: 1099,
          currency: '₽'
        },
      about: {
        title: 'Сверхъестественное. Подлинная история братьев',
        link: '/books/5',
        img: '/sources/books/Supernatural.png'
      },
      author: {
        full_name: "Елизавета Бута",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 1.5,
      reviews: 41,
      id: 5,
    },
    {
      price: {
          value: 0,
          currency: '₽'
        },
      about: {
        title: 'Тайна жожеков с красной планеты',
        link: '/books/6',
        img: '/sources/books/placholder.png'
      },
      author: {
        full_name: "Социал-шаурмист",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 5,
      reviews: 99999999,
      id: 6,
    },
    {
      price: {
          old_value: 2099,
          value: 1099,
          currency: '₽'
        },
      about: {
        title: 'Сверхъестественное. Подлинная история братьев',
        link: '/books/7',
        img: '/sources/books/Supernatural.png'
      },
      author: {
        full_name: "Елизавета Бута",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 3,
      reviews: 41,
      id: 7,
    },
    {
      price: {
          value: 0,
          currency: '₽'
        },
      about: {
        title: 'Тайна жожеков с красной планеты',
        link: '/books/6',
        img: '/sources/books/placholder.png'
      },
      author: {
        full_name: "Социал-шаурмист",
        link: "/books?author=Елизавета%20Бута"
      },
      rating: 5,
      reviews: 99999999,
      id: 8,
    },
  ].slice(0, 5)
</script>

