<script>
export default {
    name: "Header",
}
</script>

<template>
    <header class="position-fixed">
        <div class="container">
            <div class="row-1 flex">
                <div class="col-33-1">
                    <a class="white-text" href="">Donna</a>
                    <a class="white-text margin-y-10" href="">Uomo</a>
                    <a class="white-text" href="">Bambini</a>
                </div>
                <div class="col-33-1 justify-center ">
                    <img class="logo-img" src="../assets/img/boolean-logo.png" alt="Logo Boolean">
                </div>
                <div class="col-33-1 justify-right">
                    <a href=""><img class="small-image-style" src="https://img.icons8.com/forma-thin/24/user.png" alt="user"/></a>
                    <a href=""><img class="small-image-style margin-y-10" src="https://img.icons8.com/ios/50/like--v1.png" alt="heart"/></a>
                    <a href=""><img class="small-image-style" src="https://img.icons8.com/ios-filled/50/shopping-bag.png" alt="shopping-bag"/></a>
                </div>
            </div>
        </div>
    </header>
</template>