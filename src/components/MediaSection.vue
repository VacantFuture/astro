<template>
    <section class="cf mw9 center mt4-ns">
        <div class="fl w-100 w-50-ns pt2-ns">
            <!-- <article v-for="article in mediaflag" :key="article.id" class="bb b--black-10">
    
                <a class="db pv4 ph3 ph0-l no-underline black dim" href="#0">
                    
                    <div class="flex flex-column flex-row-ns">
                        <div class="pr3-ns mb4 mb0-ns w-100 w-40-ns">
                            <img :src="article.cover.url" class="db"
                                alt="Photo of a whale's tale coming crashing out of the water."/>
                        </div>
                        <div class="w-100 w-60-ns pl3-ns">
                            <h1 class="f3 fw1  mt0 lh-title">{{article.title}}</h1>
                            <p class="f6 f5-l lh-copy">
                                
                                {{article.SeoMeta.content}}
                            </p>
                            <p class="f6 lh-copy mv0">By Robin Darnell</p>
                            <p class="f-subhead  pa1 bg-near-white ba b--light-blue br2 lh-copy mt3" style="width: fit-content">{{ article.category.selection}}</p>
                        </div>
                    </div>
                </a>
            </article> -->

            <article class="bb b--black-10">
                <a class="db pv4 ph3 ph0-l no-underline black dim" href="#0">
                    <div class="flex flex-column flex-row-ns">
                        <div class="pr3-ns mb4 mb0-ns w-100 w-30-ns">
                            <img src="http://mrmrs.github.io/photos/cpu.jpg" class="db"
                                alt="Photo of a dimly lit room with a computer interface terminal.">
                        </div>
                        <div class="w-100 w-60-ns pl3-ns">
                            <h1 class="f3 fw1  mt0 lh-title">Tech Giant Invests Huge Money to Build a
                                Computer
                                Out of Science Fiction</h1>
                            <p class="f6 fw3 f5-l lh-copy">
                                The tech giant says it is ready to begin planning a quantum
                                computer, a powerful cpu machine that relies on subatomic particles instead
                                of transistors.
                            </p>
                            <p class="f6 lh-copy mv0">By Robin Darnell</p>
                        </div>
                    </div>
                </a>
            </article>
            <article class="bb b--black-10">
                <a class="db pv4 ph3 ph0-l no-underline black dim" href="#0">
                    <div class="flex flex-column flex-row-ns">
                        <div class="pr3-ns mb4 mb0-ns w-100 w-30-ns">
                            <img src="http://mrmrs.github.io/photos/warehouse.jpg" class="db"
                                alt="Photo of a warehouse with stacked shelves.">
                        </div>
                        <div class="w-100 w-60-ns pl3-ns">
                            <h1 class="f3 fw1  mt0 lh-title">Warehouse Prices Are Fast on the Rise</h1>
                            <p class="f6 f5-l lh-copy">
                                A warehouse is a commercial building for storage of goods.
                                Warehouses are used by manufacturers, importers, exporters,
                                wholesalers, transport businesses, customs, etc. They are
                                usually large plain buildings in industrial areas of cities,
                                towns and villages.
                            </p>
                            <p class="f6 lh-copy mv0">By Robin Darnell</p>
                        </div>
                    </div>
                </a>
            </article>
            <article class="bb b--black-10">
                <a class="db pv4 ph3 ph0-l no-underline black dim" href="#0">
                    <div class="flex flex-column flex-row-ns">
                        <div class="pr3-ns mb4 mb0-ns w-100 w-30-ns">
                            <img src="http://mrmrs.github.io/photos/whale.jpg" class="db"
                                alt="Photo of a whale's tale coming crashing out of the water.">
                        </div>
                        <div class="w-100 w-60-ns pl3-ns">
                            <h1 class="f3 fw1  mt0 lh-title">Giant Whale Invests Huge Money to Build a
                                Computer
                                Out of Plankton</h1>
                            <p class="f6 f5-l lh-copy">
                                Whale is the common name for a widely distributed and diverse
                                group of fully aquatic placental marine mammals. They are an
                                informal grouping within the infraorder Cetacea, usually
                                excluding dolphins and porpoises.
                            </p>
                            <p class="f6 lh-copy mv0">By Robin Darnell</p>
                        </div>
                    </div>
                </a>
            </article>
        </div>
        <div class="fl w-100 w-40-ns pl4-ns pt2-ns">
            <SmNewsletter/>
            <AD300x600/>
        </div>
    </section>
</template>
<script>
export default {
    //flow/feed, featureImage not NULL, offset by two, limit=3
    async fetch() {
        this.mediaflag = await fetch(
            'http://localhost:1337/articles?placement.flow=mediaflag&_sort=published_at:ASC&_limit=3',
             ).then((res) => res.json())
    },
    data(){
        return {
            mediaflag: {}
        }
    },
    
}

</script>
