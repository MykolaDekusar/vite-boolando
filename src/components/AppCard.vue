<script>
import list from '../data/db.json'
export default {
    name: "Card",
    data() {
        return {
            cards: list.products,
        }
    },
    methods: {
        checkDiscount(badges){
            for(let i =0; i<badges.length; i++){
                if(badges[i].type==="discount"){
                    return badges[i].value;
                } 
            }
        },
        checkTag(badges){
            for(let i =0; i<badges.length; i++){
                if(badges[i].type==="tag"){
                    return badges[i].value;
                } 
            }
        }
    }
};
</script>

<template>
    <div class="col-33-2" v-for = "card in cards">
        <div class="content position-relative">
            <img class="main-img" :src="'/img/' + card.frontImage" :alt="card.brand + ' Brand'">
            <img class="hover-img" :src="'/img/' + card.backImage" :alt="card.brand + ' Brand'">
            <div class="badges">
                <div v-if="checkDiscount(card.badges)" class="discount red white-text weight-700 small-text">{{checkDiscount(card.badges)}}</div>
                <div v-if="checkTag(card.badges)" class="green sostenibilità white-text weight-700 small-text">{{checkTag(card.badges)}}</div>
            </div>
            <div :class="{redHeart: card.isInFavorites}" class="heart white">&hearts;</div>
            <p>{{card.brand}}</p>
            <h2>{{card.name}}</h2>
            <p><span class="weight-700 red-text ">{{ card.price }} &euro;</span></p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '/src/assets/snippets/colors' as *;
/* ON IMAGE TAGS */
.badges {
    position:absolute;
    left: 0;
    bottom: 110px;
    display: flex;
    
        .sostenibilità {
        padding: 5px 10px;
        }
        .discount {
            margin-right: 5px;
        padding: 5px 10px;
        }
}

/* CONTENT */
.content img {
    width: 100%;
}

// IMG SETUP
.img-fit {
    object-fit: fill;
}

/* HOVER SETUP */
.hover-img {
    display: none;
}

.content:hover .main-img {
    display: none;
}

.content:hover .hover-img {
    display: inline-block;
}

/* DISCOUNTS */
.gray-text-crossed {
    color: $gray;
    text-decoration: line-through;
}

/* HEART SETTINGS */
.heart {
    position: absolute;
    top: 10px;
    right: 0;
    padding: 5px 15px;
    font-size: 30px;
}

.heart:hover {
    color: $red;
}

.redHeart {
    color: $red;
}
</style>