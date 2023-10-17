<template>
    <!-- top navbar -->
    <nav v-motion-fade-visible-once class="absolute px-4 lg:px-32 w-full h-20 flex items-center justify-between z-40">
        <div class="flex items-center justify-start w-44">
            <nuxt-img :src="route.fullPath == '/' ? '/img/gsi-logo mono-v2.png' : '/img/gsi-logo-v2.png'" format="webp" loading="lazy" sizes="sm:20vw" class="object-cover object-center h-16"/>
        </div>
        <div class="hidden lg:block">
            <ul :class="route.fullPath == '/' ? 'text-gsi-gold' : ''" class="flex gap-x-8 font-oswald tracking-wide">
                <li v-for="(item, index) in menu" :key="index">
                    <nuxt-link :to="item.link">
                        {{ item.name }}
                    </nuxt-link>
                </li>
            </ul>
        </div>
        <div class="flex items-center justify-end w-44">
            <ButtonBaseSmall class="gold">
                <Icon name="lucide:phone-call" class="text-xl" />
                Kontak Kami
            </ButtonBaseSmall>
        </div>
    </nav>
</template>

<script setup lang="ts">
const route = useRoute()

const storeMenu = useMenuStore()

const {
    menu
} = storeToRefs(storeMenu)

</script>

<style scoped>

</style>