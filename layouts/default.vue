<template>
    <div id="wrapper" class="mr-40 ml-40 mt-20">
        <app-header></app-header>
        <div id="content-wrapper">
            <div id="content">
                <nuxt/>
            </div>
        </div>
        <app-footer></app-footer>
    </div>
</template>
  
<script>
    import Header from "~/components/layouts/Header.vue";
    import Footer from "~/components/layouts/Footer.vue";
    export default {
        components: {
            'app-header': Header,
            'app-footer': Footer,
        }
    }
</script>