<template>
<div>
<!-- <p>
    {{ indexfeed }}
</p> -->
    <ul class="list">
                <li class="ph3 pt0 pb4-ns pb3 ph4-ns bb b--black-10">
                    <h3 class="db f3 mb1">alignment</h3>
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
                        The part of lowercase letters (such as k, b, and d) that ascends above the
                        x-height of the other lowercase letters in a face.
                    </span>
                </li> 
<li v-for="article in indexfeed" :key="article.id" class="pa3 pb4-ns pb3 ph4-ns bb b--black-10 lh-copy measure">
    <b class="db f3 mb1">{{ article.attributes.title }}</b>
    <!-- <span class="f5 db lh-copy measure">{{ article.SeoMeta.content }}</span> -->
</li>
            </ul>
            </div>
</template>
<script>
export default {
    
    async fetch() {
        
        const data = await fetch(
            'http://localhost:1337/api/articles',
        ).then((res) => res.json())
             this.indexfeed = data.data
    },
    
    data(){
        return {
            indexfeed: {},
            
        }
    }
}

</script>
