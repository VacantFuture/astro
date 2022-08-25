<template>
    <section class="cf mw9 center mb4-ns mt5-ns">
        <div class="fl w-100 w-50-ns">
            <div class="aspect-ratio aspect-ratio--4x3 mb4">
            <div class="dt aspect-ratio--object cover" style="z-index:-1;background:url(https://nsbasetest.s3.amazonaws.com/Cranberry_Lake%2C_Black_Duck_Hole%2C_Wanakena%2C_NY.jpg) center;"></div>
                <div class="dtc v-mid">
                    <header class="white-70">
                        <!-- <h2 class="f6 fw1 ttu tracked mb2 lh-title">{{ featured.published }}</h2> -->
                        <!-- <h3 class="f6 fw1 lh-title">{{ featured.title }}</h3> -->
                    </header>
                    <h1 class="f3 measure fw1 i white-60">{{ featured.title }}</h1>
                    <blockquote class="ph0 mh0 measure f4 lh-copy center">
                        <p class="fw1 white-70">
                            {{ featured.published }}
                        </p>
                        <cite class="f6 ttu tracked fs-normal">Massimo Vignelli</cite>
                    </blockquote>
                </div>
            </div>
        </div>
        <div class="fl w-100 w-40-ns">
            <ul class="list fr">
                <li class="ph3 pt0 pb4-ns pb3 ph4-ns bb b--black-10">
                    <b class="db f3 mb1">alignment</b>
                    <span class="f5 db lh-copy measure">
                        The positioning of text within the page margins. Alignment can be flush left, flush right,
                        justified, or centered. Flush left and flush right are sometimes referred to as left justified
                        and right justified.</span>
                </li>
                <li class="pa3 pa4-ns bb b--black-10">
                    <b class="db f3 mb1">
                        ascender
                    </b>
                    <span class="f5 db lh-copy measure">
                       {{ feed[0] }}
                    </span>
                </li>

            </ul>
            <div class="pa4-ns">
                <img src="https://via.placeholder.com/300x250.png" class="pl4-ns ml2" alt="">
            </div>
        </div>
    </section>
</template>
<script>
export default {
    // localhost:1337/api/flows?filters[Placement][$eq]=Feature&populate=%2a

    //limit two on flow/feed, starting at zero
    async fetch() {
        this.featured = await fetch(
            'http://localhost:1337/api/getFeature',
        ).then((res) => res.json());

        this.feed = await fetch(
            'http://localhost:1337/api/getFeed'
        ).then((res) => res.json());
             
    },
    data(){
        return {
            featured: {},
            feed: []
                     }
        
    },
    computed:{
    styleObject: function() {
                return this.featured.url
             }
    
}
}
</script>