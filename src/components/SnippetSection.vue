<template>
    <section class="cf mw9 center mt4-ns">
        <div class="fl w-100 w-60-ns pt2-ns">

            <Snippet/>
        </div>
        <div class="fl w-100 w-40-ns pl4-ns pt2-ns">
           <TextFeed :count="4"/>
            <div class="pa4-ns">
                <img src="https://via.placeholder.com/300x250.png" class="pl4-ns ml2" alt="">
            </div>
        </div>
    </section>
</template>
<script>
