<script>
export default {
    name: "Card",
    data() {
        return {
            cards: [
                {
                    mainImg: "/public/img/1.webp",
                    offImg : "/public/img/1b.webp",
                    brand: "Levi's",
                    name: "RELAXED FIT TEE UNISEX",
                    price:"14.99",
                    discPrice: "29.99",
                    discPerc:"50%",
                    sus:true,
                },
                {
                    mainImg: "/public/img/2.webp",
                    offImg : "/public/img/2b.webp",
                    brand: "Guess",
                    name: "ROSES TEE",
                    price:"20,99",
                    discPrice: "29.99",
                    discPerc:"30%",
                    sus: false,
                },
                {
                    mainImg: "/public/img/3.webp",
                    offImg : "/public/img/3b.webp",
                    brand: "Come Zucchero Filato",
                    name: "VOGLIA DI COLORI PASTELLO",
                    price:"129,99",
                    discPrice: "184,99",
                    discPerc:"30%",
                    sus:false,
                },
                {
                    mainImg: "/public/img/4.webp",
                    offImg : "/public/img/4b.webp",
                    brand: "Levi's",
                    name: "TEE UNISEX",
                    price:"14.99",
                    discPrice: "29.99",
                    discPerc:"50%",
                    sus:true,
                },
                {
                    mainImg: "/public/img/5.webp",
                    offImg : "/public/img/5b.webp",
                    brand: "Maya Deluxe",
                    name: "STRIPE BODICE",
                    price:"99,99",
                    discPrice: "",
                    discPerc:"",
                    sus:false,
                },
                {
                    mainImg: "/public/img/6.webp",
                    offImg : "/public/img/6b.webp",
                    brand: "Esprit",
                    name: "MAGLIONE - BLACK",
                    price:"29,99",
                    discPrice: "",
                    discPerc:"",
                    sus:true,
                },
                
            ]
        }
    }
};
</script>

<template>
    <div class="col-33-2" v-for = "card in cards">
        <div class="content position-relative">
            <img class="main-img" :src="card.mainImg" :alt="card.brand + ' Brand'">
            <img class="hover-img" :src="card.offImg" :alt="card.brand + ' Brand'">
            <div v-if="card.discPerc" class="discount red white-text weight-700 small-text">-{{ card.discPerc }}</div>
            <div v-if="card.sus" :class="{sostenibilità : card.sus, discount : !card.discPerc}" class="green white-text weight-700 small-text">Sostenibili&agrave;</div>
            <div class="heart white">&hearts;</div>
            <p>{{card.brand}}</p>
            <h2>{{card.name}}</h2>
            <p><span class="weight-700 red-text ">{{ card.price }} &euro;</span> <span v-if="card.discPrice" class="gray-text-crossed">{{ card.discPrice }} &euro;</span></p>
        </div>
    </div>
</template>