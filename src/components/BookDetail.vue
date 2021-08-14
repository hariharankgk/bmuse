<template>
  <div class="book_detail">
      <div class="book_detail__main">
          <h3 class="book_detail__main__title">{{book.title}}</h3>
          <img :src="require('../assets/books/' + book.book_image)" class="book_detail__main__image"/>
          <br/>
          <button type="button" class="book_detail__main__favourite">Add to Favourites &nbsp;&nbsp;&nbsp;+</button>
      </div>
      <div class="book_detail__info">
          <h4 class="book_detail__author">{{book.author}}</h4>
          <h5 class="book_detail__publisher">{{book.publisher}}</h5>
          <p class="book_detail__description">{{book.description}}</p>
      </div>
      <div class="book_detail__close">
          <a href="#" @click.prevent="$emit('closeBook')">
              <img src="../assets/close.png" alt="close">
          </a>
      </div>
  </div>
</template>

<script>
export default {
  name: 'BookDetail',
  props: {
      book: Object
  }
}
</script>

<style scoped lang="scss">
    .book_detail {
        padding: 20px;
        position: relative;
        @media (min-width: 768px) {
            display: flex;
            padding: 50px;
            justify-content: space-between;
        }
        .book_detail__main {
            @media (min-width: 768px) {
                width: 30%;
            }
            .book_detail__main__title {
                font-size: 40px;
                font-weight: 100;
                font-stretch: normal;
                font-style: normal;
                line-height: 1.2;
                letter-spacing: .6px;
                color: #c3a572;
                margin-bottom: 40px;
                margin-top: 0;
                max-width: 360px;
                text-align: left;
            }

            .book_detail__main__image {
                width: 60px;
                border-radius: 4px;
                object-fit: cover;
            }

            .book_detail__main__favourite {
                width: 250px;
                padding: 10px 30px;
                background-color: #282a2c;
                color: #fff;
                margin-top: 30px;
                box-shadow: none;
                border: none;
                outline: 0;
                font-size: 16px;
                border-radius: 5px;
            }
        }

        .book_detail__info {
            margin-top: 30px;
            @media (min-width: 768px) {
                width: 50%;
                margin-top: 0;
            }
            .book_detail__author {
                font-size: 18px;
                font-weight: 500;
                font-stretch: normal;
                font-style: normal;
                line-height: normal;
                letter-spacing: normal;
                color: #fff;
                margin: 0;
                margin-bottom: 2px;
            }

            .book_detail__publisher {
                font-size: 14px;
                font-weight: 300;
                font-stretch: normal;
                font-style: normal;
                line-height: 1.44;
                letter-spacing: .43px;
                color: hsla(0,0%,100%,.6);
                margin: 0;
            }

            .book_detail__description {
                font-size: 14px;
                font-weight: 300;
                font-stretch: normal;
                font-style: normal;
                line-height: 1.36;
                letter-spacing: .4px;
                color: hsla(0,0%,100%,.7);
                padding: 0;
                padding-right: 50px;
                padding-top: 30px;
                word-break: break-word;
            }
        }

        .book_detail__close {
            @media (max-width: 767px) {
                position: absolute;
                top: 0;
                right: 20px;
            }
        }
    }
</style>
