<template>
    <div class="relative overflow-hidden">
        <Navbar />
        <!-- hero section -->
        <div class="relative min-h-screen bg-slate-800 px-4 lg:px-32 pt-40 overflow-hidden">
            <div class="flex flex-col items-center gap-4 justify-center h-full">
                <div v-motion-fade-visible-once class="text-center space-y-3 z-10">
                    <div>
                        <h1 class="font-oswald text-6xl lg:text-9xl text-gsi-gold tracking-tighter">Griya</h1>
                        <h1 class="font-oswald text-6xl lg:text-9xl text-gsi-gold tracking-tighter">Sambirejo Indah</h1>
                    </div>
                    <h3 class="font-oswald text-xl lg:text-4xl text-gsi-smokewhite">Best Affordable Modern Home at Jombang</h3>
                    <p class="text-xs lg:text-base text-gsi-smokewhite">Mengusung konsep minimalis modern yang terjangkau, dapatkan hunian impian anda bersama kami</p>
                </div>
                <div v-motion-slide-visible-once-bottom :delay="500" class="relative rounded-lg z-20 my-12 lg:px-56">
                    <video class="rounded-3xl shadow-md" autoplay loop muted>
                        <source src="/bumper.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                    <div class="flex pt-3 gap-3">
                        <div class="lg:absolute right-0 top-16 rounded-3xl lg:border-8 border-slate-800 overflow-hidden lg:shadow-md">
                            <nuxt-img src="/img/gsi03.jpeg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center h-44 w-full"/>
                        </div>
                        <div class="lg:absolute left-0 bottom-16 rounded-3xl lg:border-8 border-slate-800 overflow-hidden lg:shadow-md">
                            <nuxt-img src="/img/gsi01.jpeg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center h-44 w-full"/>
                        </div>
                    </div>
                </div>
            </div>
            <p class="absolute py-10 -right-56 opacity-20 md:opacity-50 top-10">
                <Icon name="PatternThree" class="text-[28rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
            <p class="absolute py-10 -left-56 opacity-20 md:opacity-50 bottom-40">
                <Icon name="PatternThree" class="text-[28rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
        </div>

        <!-- about section -->
        <div v-motion-slide-visible-once-bottom :delay="300" class="grid grid-cols-6 items-center gap-6 px-4 lg:px-32 py-10">
            <div class="relative flex gap-4 justify-between items-center col-span-6 lg:col-span-2 rounded-xl">
                <nuxt-img src="/img/gsi tes.png" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center rounded-xl shadow-md"/>
                <div class="lg:bg-gsi-gold lg:absolute lg:hover:scale-125 transition-all duration-300 flex items-center justify-center h-32 -top-16 -right-16 p-3 rounded-xl lg:shadow-md">
                    <nuxt-img src="/img/gsi-logo-v2.png" format="webp" loading="lazy" sizes="sm:20vw" class="object-cover object-center rounded-xl h-32 lg:h-28"/>
                </div>
            </div>
            <div class="col-span-6 lg:col-span-4 flex flex-col gap-3 lg:gap-4 lg:pl-6">
                <h3 class="font-oswald text-3xl lg:text-4xl tracking-tight text-gsi-darkblue">Sekilas Tentang Kami</h3>
                <p class="text-sm lg:text-base text-justify">Griya Sambirejo Indah adalah kawasan perumahan yang mengusung konsep hunian modern minimalis yang terjangkau. Berlokasi strategis di Desa Sambirejo, Kec. Jogoroto, Kab. Jombang, dekat dengan berbagai fasilitas umum & Jalan utama Nasional serta kurang dari 15 menit dari pusat Jombang. Segera dapatkan hunian impian anda bersama kami Griya Sambirejo Indah.</p>
                <ButtonBase class="gold mt-3">
                    Hubungi Kami
                </ButtonBase>
            </div>
        </div>

        <!-- advantages section -->
        <div v-motion-fade-visible-once :delay="400" class="relative px-4 lg:px-32 py-10 mb-6">
            <h3 class="font-oswald text-3xl lg:text-4xl tracking-tight text-gsi-darkblue text-left lg:text-center mb-3 lg:mb-4">Keunggulan Hunian Kami</h3>
            <p class="mb-6 text-left lg:text-center text-sm lg:text-base">Nikmati berbagai keunggulan yang bisa anda dapatkan di kawasan hunian kami.</p>
            <div class="relative grid grid-cols-2 lg:grid-cols-3 items-center gap-2 lg:gap-6 z-40">
                <div v-for="(item, index) in facilities" :key="index" :class="item.mode == false ? 'bg-gsi-gold text-gsi-darkblue' : 'text-gsi-gold bg-gsi-darkblue'" class="flex flex-col items-center px-2 lg:px-4 py-6 justify-center gap-2 rounded-xl shadow-md hover:scale-105 transition-all duration-300">
                    <Icon :name="item.icon" class="text-5xl" />
                    <p class="text-base lg:text-xl font-oswald">{{item.name}}</p>
                </div>
            </div>
            <div class="absolute -right-12 opacity-30 md:opacity-80 -top-48 rotate-180">
                <Icon name="PatternThree" class="text-[22rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
            <div class="absolute -left-12 opacity-30 md:opacity-80 -bottom-48 rotate-180">
                <Icon name="PatternThree" class="text-[22rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
        </div>

        <!-- location section -->
        <div v-motion-fade-visible-once :delay="300" class="relative grid grid-cols-6 items-center gap-6 px-4 lg:px-32 py-10">
            <div class="relative flex gap-4 justify-between items-center col-span-6 lg:col-span-3 rounded-xl">
                <nuxt-img src="/img/tesmaps.png" format="webp" loading="lazy" sizes="sm:100vw" class="object-cover object-center rounded-xl shadow-md"/>
                
            </div>
            <div class="col-span-6 lg:col-span-3 flex flex-col gap-3 lg:gap-4 lg:pl-6">
                <h3 class="font-oswald text-3xl lg:text-4xl tracking-tight text-gsi-darkblue">Lokasi Strategis</h3>
                <p class="text-sm lg:text-base text-justify">Griya Sambirejo Indah berada di lokasi yang strategis & menjadi pilihan tepat bagi anda yang menginginkan hunian dengan suasana nyaman, jauh dari kebisingan, namun dekat dengan berbagai fasilitas publik penunjang kebutuhan anda.</p>
                <ul class="list-inside list-disc">
                    <li v-for="(item, index) in locations" :key="index" class="font-oswald tracking-wide">
                        {{ item.distance }} {{ item.name }}
                    </li>
                </ul>
            </div>
            <div class="absolute -right-8 opacity-30 md:opacity-80 top-44 rotate-180">
                <Icon name="PatternThree" class="text-[22rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
        </div>

        <!-- promotion section -->
        <div v-motion-slide-visible-once-bottom class="relative px-4 lg:px-32 py-16 bg-gray-800 overflow-hidden mb-10">
            <div class="text-center z-50 relative">
                <h3 class="font-oswald text-2xl lg:text-4xl text-gsi-smokewhite mb-4">Harga Start From</h3>
                <div class="flex gap-2 lg:gap-3 justify-center items-end">
                    <h2 class="font-oswald text-6xl lg:text-8xl text-gsi-gold tracking-tighter">Rp. 200</h2>
                    <h3 class="font-oswald text-3xl lg:text-6xl text-gsi-gold tracking-tighter">Jutaan * / Unit</h3>
                </div>
                <p class="text-sm lg:text-lg text-gsi-smokewhite mt-4 lg:mt-8 lg:px-28">Dapatkan berbagai penawaran dan promo menarik khusus untuk anda, yang bisa anda dapatkan untuk pemesanan unit hunian kami saat ini. Segera booking sekarang juga sebelum kehabisan, kunjungi kantor pemasaran atau kontak kami untuk informasi lebih lanjut.</p>
                <ButtonBase class="gold mt-6 shadow-md">
                    Booking Sekarang
                </ButtonBase>
            </div>
            <div class="absolute opacity-10 top-0 left-0 z-10">
                <nuxt-img src="/img/gsi01.jpeg" format="webp" loading="lazy" sizes="sm:50vw" class="object-cover object-center h-screen shadow-md lg:h-auto lg:w-screen z-10"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
            <div class="absolute -left-44 opacity-20 md:opacity-80 -top-10">
                <Icon name="PatternThree" class="text-[22rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
            <div class="absolute -right-44 opacity-20 md:opacity-80 bottom-0">
                <Icon name="PatternThree" class="text-[22rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
        </div>

        <!-- contact section -->
        <ContactSection />
    </div>
</template>

<script setup lang="ts">

const storeGlobalData = useGlobalDataStore()

const {
    facilities,
    locations
} = storeToRefs(storeGlobalData)


</script>

<style scoped>

</style>