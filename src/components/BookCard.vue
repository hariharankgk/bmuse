<template>
  <div class="book_card">
      <img class="book_card__imgae" :src="require('../assets/books/' + book.book_image)">
      <div class="book_card__overlay">
        <div class="book_card__top">
            <p class="book_card__top__rating">{{book.rating}} out of 5</p>
        </div>
        <div class="book_card__bottom">
            <h4 class="book_card__bottom__title">{{book.title}}</h4>      
            <p class="book_card__bottom__author">{{book.author}}</p>
            <p class="book_card__bottom__publisher">{{book.publisher}}</p>
        </div>      
    </div>
  </div>
</template>

<script>
export default {
  name: 'BookCard',
  props: {
      book: Object
  }
}
</script>

<style scoped lang="scss">
    .book_card {
        position: relative;
        box-shadow: 0 0 15px #00000045;
        .book_card__imgae {
            max-width: 100%;
            border-radius: 15px;
        }
        .book_card__overlay {
            position: absolute;
            top: 0;
            right: 0;
            left:0;
            bottom: 0;
            z-index: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            background-color: rgba(0, 0, 0, .4);
            border-radius: 15px;
        }
        .book_card__top {
            text-align: right;
            .book_card__top__rating {
                margin: 0;
                padding: 5px 10px;
                display: inline-block;
                background: #003366;
                opacity: 0.90;
                font-size: 16px;
                color: #fff;
                font-weight: 400;
                border-radius: 0 15px 0 15px;
                font-stretch: normal;
                font-style: normal;
                line-height: normal;
                letter-spacing: .2px;
            }   
        }

        .book_card__bottom {
            padding: 0 10px 10px;
            .book_card__bottom__title {
                font-size: 18px;
                font-weight: 500;
                font-stretch: normal;
                font-style: normal;
                line-height: 1.2;
                letter-spacing: -.2px;
                color: #fff;
                max-width: 100%;
                margin: 0;
                margin-bottom: 5px;
                text-transform: capitalize;
            }

            .book_card__bottom__author, .book_card__bottom__publisher {
                font-size: 13px;
                font-weight: 300;
                font-stretch: normal;
                font-style: normal;
                line-height: 1.4;
                margin: 0;
                letter-spacing: .4px;
                color: hsla(0,0%,100%,.9);
            }
        }

    }
</style>
