<script>
export default {
    name: "Header",
    data(){
        return {
            headerOptions: [
                {
                    sel1:"Donna",
                    sel2:"Uomo",
                    sel3:"Bambini"
                },
            ],
            logoImg: "/img/boolean-logo.png",
            headerIcons: [
            {
                source1: "https://img.icons8.com/forma-thin/24/user.png",
                alt1:"User",
            
                source2: "https://img.icons8.com/ios/50/like--v1.png",
                alt2:"Heart",
            
                source3: "https://img.icons8.com/ios-filled/50/shopping-bag.png",
                alt3:"Shopping-bag",
            },
           ],
        }
    }
};
</script>

<template>
    <header class="position-fixed">
        <div class="container">
            <div class="row-1 flex">
                <div class="col-33-1" v-for="opz in headerOptions">
                    <a class="white-text" href="">{{opz.sel1}}</a>
                    <a class="white-text margin-y-10" href="">{{opz.sel2}}</a>
                    <a class="white-text" href="">{{opz.sel3}}</a>
                </div>
                <div class="col-33-1 justify-center ">
                    <img class="logo-img" :src="this.logoImg" alt="Logo Boolean">
                </div>
                <div class="col-33-1 justify-right" v-for = "icons in headerIcons">
                    <a href=""><img class="small-image-style" :src="icons.source1" :alt="icons.alt1"/></a>
                    <a href=""><img class="small-image-style margin-y-10" :src="icons.source2" :alt="icons.alt2"/></a>
                    <a href=""><img class="small-image-style" :src="icons.source3" :alt="icons.alt3"/></a>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '/src/assets/snippets/colors' as *;

header {
    background-color: $header-color;
    padding: 10px 0;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1;

    .logo-img {
    width: 100px;
}
}
</style>