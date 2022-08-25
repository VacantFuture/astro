<template>
    <section class="cf mw9 center mt4-ns">
        <div class="fl w-100 w-60-ns pt2-ns">

            <TextFeed :count="4"/>
          
        </div>
        <div class="fl w-100 w-40-ns pl4-ns pt2-ns">
            <ul class="list">
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
                        The part of lowercase letters (such as k, b, and d) that ascends above the
                        x-height of the other lowercase letters in a face.
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
