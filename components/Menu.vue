<template>
    <div @click="toggleMenu" class="cursor-pointer relative">
        <div class="min-w-[92px]">
            <span class="uppercase font-bold">Menu</span>
            <MenuIcon v-if="!showMenu" class="w-10 h-10"/>
            <CloseIcon v-if="showMenu" class="w-10 h-10"/>
        </div>
        <div v-if="showMenu" class="absolute right-1 top-12">
            <ul class="menu">
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/">About Us</nuxt-link></li>
                <li @click.stop="toggleSubLink"><nuxt-link to="#"><span>Services</span></nuxt-link> <ChevronDown v-if="!showSubLink"/><ChevronUp v-if="showSubLink"/></li>
                    <ul v-if="showSubLink" class="subMenu">
                        <li> <nuxt-link to="/"> Rehabs</nuxt-link></li>
                        <li><nuxt-link to="/">Short Term Rentals</nuxt-link></li>
                        <li><nuxt-link to="/">Home Studios</nuxt-link></li>
                    </ul>
                <li><nuxt-link to="/">Markets</nuxt-link></li>
                <li><nuxt-link to="/">Contact Us</nuxt-link></li>
            </ul>
        </div>
    </div>
</template>

<script>
import MenuIcon from './icons/MenuIcon.vue';
import CloseIcon from './icons/CloseIcon.vue';
import ChevronUp from './icons/ChevronUpIcon.vue';
import ChevronDown from './icons/ChevronDownIcon.vue';
export default {
    components: {
    MenuIcon,
    CloseIcon,
    ChevronUp,
    ChevronDown,
},
    data() {
        return {
            showMenu: false,
            showSubLink: false,
        }
    },
    methods: {
        toggleMenu() {
            this.showMenu = !this.showMenu
        },
        toggleSubLink() {
            this.showSubLink = !this.showSubLink
        }
    }
}
</script>

<style>

</style>