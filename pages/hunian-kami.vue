<template>
    <div class="relative overflow-hidden">
        <Navbar />
        <div v-motion-slide-visible-once-bottom class="relative mt-24 lg:mt-32  px-4 lg:px-32 py-10">
            <h3 class="font-oswald text-3xl lg:text-5xl tracking-tight text-gsi-darkblue mb-4 text-center"><span class="text-gsi-gold">Tipe</span> Hunian Kami</h3>
            <p class="mb-6 text-left lg:text-center text-sm lg:text-base">Pilih tipe hunian kami yang paling sesuai dengan keinginan anda sekarang.</p>
            <div class="relative z-30 grid grid-cols-12 rounded-xl items-start gap-6">
                <!-- begin card v3 -->
                <div class="col-span-6 relative w-full border bg-white transition-all duration-300 rounded-md">
                    <!-- top card v3 -->
                    <div class="flex flex-col items-center border-b p-6 sm:flex-row">
                        <div class="flex flex-col items-center gap-3 sm:flex-row">
                            <Avatar class="lg">
                                <nuxt-img src="/img/ava01.png" format="webp" loading="lazy" sizes="sm:20vw" class="object-cover object-center h-20 w-20 rounded-full" />
                            </Avatar>
                            <div class="text-center sm:text-left">
                                <h4 class="font-medium leading-tight">
                                    Mbingkamp Syy
                                </h4>
                                <p class="text-sm text-gray-400">
                                    Software Engineer
                                </p>
                            </div>
                        </div>
                        <div class="mt-4 flex items-center gap-3 sm:mt-0 sm:ms-auto">
                            <ButtonIcon class="mono xs shadow-md">
                                <Icon name="lucide:instagram" />
                            </ButtonIcon>
                            <ButtonIcon class="mono xs shadow-md">
                                <Icon name="lucide:twitter" />
                            </ButtonIcon>
                            <ButtonIcon class="mono xs shadow-md">
                                <Icon name="lucide:facebook" />
                            </ButtonIcon>
                            <ButtonIcon class="mono xs shadow-md">
                                <Icon name="lucide:linkedin" />
                            </ButtonIcon>
                        </div>
                    </div>
                    
                    <!-- bottom card v3 -->
                    <div class="flex flex-col items-center justify-between px-6 py-4 sm:flex-row">
                        <div class="w-full grow space-y-1 sm:w-auto sm:max-w-[260px]">
                            <div class="flex items-center justify-between">
                                <h4 class="text-sm">
                                    Progress
                                </h4>
                                <p class="text-gray-400 text-sm">
                                    12%
                                </p>
                            </div>
                            <div role="progressbar" aria-valuenow="12" aria-valuemax="100" class="relative w-full overflow-hidden h-1 rounded-full bg-gray-400">
                                <div class="absolute start-0 top-0 h-full transition-all duration-300 bg-sky-500 rounded-full" style="width: 12%;"></div>
                            </div>
                        </div>
                        <div class="mt-4 w-full sm:mt-0 sm:w-auto">
                            <ButtonBaseExpanded class="mono">
                                View Profile
                            </ButtonBaseExpanded>
                        </div>
                    </div>
                </div>
            </div>
            <p class="absolute py-10 -right-56 opacity-20 md:opacity-50 top-10">
                <Icon name="PatternThree" class="text-[28rem] rotate-180"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
            <p class="absolute py-10 -left-56 opacity-20 md:opacity-50 bottom-40">
                <Icon name="PatternThree" class="text-[28rem] rotate-180"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
        </div>
        <div v-motion-slide-visible-once-bottom class="relative mt-10 px-4 lg:px-32 py-10">
            <div class="relative z-30 grid grid-cols-12 rounded-xl items-start gap-6">
                <div class="relative col-span-12 lg:col-span-5">
                    <div class="grid grid-cols-2 gap-2 p-2">
                        <div class="rounded-xl overflow-hidden">
                            <nuxt-img src="/img/gsi01.jpeg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center w-full"/>
                        </div>
                        <div class="rounded-xl overflow-hidden">
                            <nuxt-img src="/img/gsi02.jpeg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center w-full"/>
                        </div>
                        <div class="col-span-2 rounded-xl overflow-hidden">
                            <nuxt-img src="/img/siteplan01.jpg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center w-full"/>
                        </div>
                        <div class="rounded-xl overflow-hidden">
                            <nuxt-img src="/img/gate 1.jpg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center w-full"/>
                        </div>
                        <div class="rounded-xl overflow-hidden">
                            <nuxt-img src="/img/gsi03.jpeg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center w-full"/>
                        </div>
                    </div>
                </div>
                <div class="col-span-12 lg:col-span-7 flex flex-col gap-3 lg:gap-4 lg:pl-6">
                    <h3 class="font-oswald text-3xl lg:text-5xl tracking-tight text-gsi-darkblue mb-4"><span class="text-gsi-gold">Spesifikasi</span> Bangunan Hunian</h3>
                    <div class="grid grid-cols-2 gap-2 lg:gap-3">
                        <div v-for="(item, index) in specifications" :key="index" class="flex flex-col items-center px-2 text-gsi-smokewhite bg-gsi-darkblue lg:px-4 py-2 justify-center rounded-xl shadow-md hover:scale-105 transition-all duration-300">
                            <p class="text-sm lg:text-lg font-oswald uppercase ">{{item.name}}</p>
                            <p class="text-xs lg:text-lg font-oswald">{{item.goods}}</p>
                        </div>
                    </div>
                </div>
            </div>
            <p class="absolute py-10 -right-56 opacity-20 md:opacity-50 top-10">
                <Icon name="PatternThree" class="text-[28rem] rotate-180"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
            <p class="absolute py-10 -left-56 opacity-20 md:opacity-50 bottom-40">
                <Icon name="PatternThree" class="text-[28rem] rotate-180"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
        </div>
        <ContactSection/>
    </div>
</template>

<script setup lang="ts">
const storeGlobalData = useGlobalDataStore()

const {
    specifications
} = storeToRefs(storeGlobalData)
</script>

<style scoped>

</style>