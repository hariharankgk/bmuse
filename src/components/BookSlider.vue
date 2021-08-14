<template>
  <div class="books_slider">
        <h2 class="books_slider__title">Hardcover Fiction</h2>
        <vue-glide
            :per-view="6"
            :gap="20"
            :breakpoints="breakpoints"
        >
            <vue-glide-slide v-for="(books, index) in booksList.books" :key="index">
                <div 
                    class="books_slider__box"
                    @click="bookDetail = books"
                >
                    <BookCard :book="books" />
                </div>
            </vue-glide-slide>
            <template slot="control">
                <div class="books_slider__arrow" data-glide-dir=">">
                    <img src="../assets/slider_arrow.png" alt="right arrow">
                </div>
            </template>
        </vue-glide>

        <BookDetail 
            v-if="bookDetail.title" 
            :book="bookDetail"
            @closeBook="bookDetail = {}" 
        />
  </div>
</template>

<script>
import BookCard from '@/components/BookCard.vue'
import BookDetail from '@/components/BookDetail.vue'
import BooksJons from '../service/books.json'
import { Glide, GlideSlide } from 'vue-glide-js'

export default {
  name: 'BookSlider',
  components: {
    BookCard,
    BookDetail,
    [Glide.name]: Glide,
    [GlideSlide.name]: GlideSlide
  },
  data () {
      return {
          booksList: BooksJons.results,
          bookDetail: {},
          breakpoints: {
            800: {
                perView: 2
            }
          }
      }
  }
}
</script>

<style scoped lang="scss">
.books_slider {
    margin-top: 50px;
    .books_slider__title {
        font-size: 22px;
        font-weight: 600;
        padding-left: 10px;
        font-stretch: normal;
        font-style: normal;
        line-height: 1.27;
        letter-spacing: 1px;
        color: #ffffff;
        @media (min-width: 768px) {
            padding-left: 50px;
        }
    }

    .books_slider__list {
        padding: 0 50px;
        display: flex;
    }
}
</style>
