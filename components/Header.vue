<template>
  <div class="w-full flex justify-between items-center text-white bg-black pl-8 pr-8">
    <div><PhoneIcon class="h-[20px] mt-[-3px]"/><a class="header_phone" href="tel:844 874 2661">844 874 2661</a></div>
    <nuxt-link to="/"><img src="/logo.jpg" alt="Blue Planet Logo" width="140px" height="50px" /></nuxt-link>
    <Menu/>
  </div>
</template>

<script>
    import PhoneIcon from "./icons/PhoneIcon.vue"
export default {
    components: {
        PhoneIcon
    }

}
</script>

<style>

</style>