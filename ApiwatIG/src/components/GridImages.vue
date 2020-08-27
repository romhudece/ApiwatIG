<template>
    <div id="grid-image">
        <div class="ui card" v-for="i in 10" :key="i">
        <div class="content">
            <div class="right floated meta">6s</div>
            <img class="ui avatar image" src="data:image/png;base64,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"> TOT
        </div>
        <div class="image">
            <img src="https://www.tot.co.th/images/default-source/default-album/products/internet-service/home-use/tot-fiber-2u/teaser-mobile-product-1080x600.png?sfvrsn=f786efc1_2">
        </div>
        <div class="content">
            <span class="right floated">
            <i class="heart outline like icon"></i>
            16555 likes
            </span>
            <i class="comment icon"></i>
            1000 comments
        </div>
        <div class="extra content">
            <div class="ui large transparent left icon input">
            <i class="heart outline icon"></i>
            <input type="text" placeholder="Add Comment...">
            </div>
        </div>
    </div>
    </div>
    
</template>

<script>
export default {
    name: 'GridImages'
}
</script>

<style>

</style>