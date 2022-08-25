<template>
    <nav class="mw9-ns center">
        <a class="link black b f-headline-ns f-subheadline-m f2 tc db mb2-m mb4-ns mb2 brand" href="/"
            title="Home">North
            Country Voice</a>
        <h2 class="link dim black f6 fw4 ttu tracked tc">For the Community</h2>
        <nav class="bt bb tc mw9 center mv4">
            <ul class="ma0 pl2">
                <li v-for="category in categories" :key="category.id" class="f6 f4-l black-80 dib pa3-ns pa2 ph4-l">
                    <span v-if="$route.name === 'index'">
                        <NuxtLink :to="{ path: 'category/' + category.attributes.Category }"
                            class="link dim dark-blue no-underline">{{ category.attributes.Category }}</NuxtLink>
                    </span><span v-else>
                        <NuxtLink :to="category.attributes.Category" class="link dim dark-blue no-underline">{{
                                category.attributes.Category
                        }}</NuxtLink>
                    </span>
                </li>
            </ul>
        </nav>
    </nav>
</template>
<script>
export default {

    async fetch() {
        const data = await fetch(
            'http://localhost:1337/api/categories',
        ).then((res) => res.json())
        this.categories = data.data
    },
    data() {
        return {
            categories: {}
        }
    },

}

</script>
