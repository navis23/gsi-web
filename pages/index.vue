<template>
    <div class="relative overflow-hidden">
        <nav v-motion-fade-visible-once class="absolute px-4 lg:px-32 w-full h-20 flex items-center justify-between z-40">
            <div class="flex items-center justify-start w-44">
                <nuxt-img src="/img/gsi-logo mono-v2.png" format="webp" loading="lazy" sizes="sm:20vw" class="object-cover object-center h-16"/>
            </div>
            <div class="hidden lg:block">
                <ul class="flex text-gsi-gold gap-x-8 font-oswald tracking-wide">
                    <li>Home</li>
                    <li>About us</li>
                    <li>Hunian Kami</li>
                    <li>Galeri</li>
                </ul>
            </div>
            <div class="flex items-center justify-end w-44">
                <ButtonBaseSmall class="gold">
                    <Icon name="lucide:phone-call" class="text-xl" />
                    Contact Us
                </ButtonBaseSmall>
            </div>
        </nav>
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
        
        <div class="relative grid grid-cols-6 items-start gap-6 px-4 lg:px-32 py-10">
            <div v-motion-slide-visible-once-left :delay="300" class="relative z-40 col-span-6 lg:col-span-3 flex flex-col gap-3 lg:gap-4 lg:pl-6  border-l-4 border-gsi-gold px-4 rounded ">
                <h3 class="font-oswald text-4xl lg:text-6xl text-gsi-darkblue tracking-tight">Segera hubungi kami & dapatkan <span class="text-gsi-gold">rumah impian</span> anda sekarang</h3>
            </div>
            <div v-motion-slide-visible-once-right :delay="300" class="relative overflow-hidden z-40 bg-gsi-smokewhite col-span-6 lg:col-span-3 flex items-center gap-4 lg:gap-8 text-gsi-darkblue border border-gray-300 shadow-md rounded-xl px-4 lg:px-8 py-6">
                <div class="flex flex-col gap-y-1 lg:gap-y-2 border-r pr-4 lg:pr-8 border-slate-300 font-oswald font-semibold text-lg lg:text-xl">
                    <p>C</p>
                    <p>O</p>
                    <p>N</p>
                    <p>T</p>
                    <p>A</p>
                    <p>C</p>
                    <p>T</p>
                </div>
                <div class="relative z-40 flex flex-col gap-3 lg:gap-4 text-gsi-darkblue">
                    <div v-for="(item, index) in contacts" :key="index" class="flex gap-x-3 items-center justify-start">
                        <Icon :name="item.icon" class="text-3xl" />
                        <p class="font-oswald text-base lg:text-xl">{{ item.description }}</p>
                    </div>
                </div>
                <div class="absolute -right-12 opacity-50 md:opacity-80 bottom-3 -rotate-90">
                    <Icon name="PatternThree" class="text-[15rem] lg:text-[16.5rem]"/>
                </div>
            </div>
            <div class="absolute -left-6 opacity-30 md:opacity-80 top-48 rotate-180">
                <Icon name="PatternThree" class="text-[22rem]"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </div>
        </div>
        <div class="relative flex flex-col lg:flex-row items-center gap-3 justify-between px-4 lg:px-32 py-4 bg-gray-800 overflow-hidden mt-10">
            <div class="flex flex-col lg:flex-row items-center gap-3">
                <nuxt-img src="/img/gsi-logo mono-v2.png" format="webp" loading="lazy" sizes="sm:20vw" class="object-cover object-center h-12"/>
                <p class="text-gsi-smokewhite text-xs lg:text-sm">
                    All Rights Reserved © Griya Sambirejo Indah, 2023
                </p>
            </div>
            <p class="text-gsi-smokewhite text-xs lg:text-sm">
                Create with passion & love by @enterbiner
            </p>
        </div>
    </div>
</template>

<script setup lang="ts">
const initial = ref({
    y: 100,
    opacity: 0,
})

const enter = ref({
    y: 0,
    opacity: 1,
})

const facilities = ref([
    {
        'id' : 1,
        'name' : 'One Gate System',
        'icon' : 'lucide:construction',
        'mode' : false
    },
    {
        'id' : 2,
        'name' : 'Modern Minimalist Home',
        'icon' : 'lucide:home',
        'mode' : true
    },
    {
        'id' : 3,
        'name' : 'Harga Terjangkau',
        'icon' : 'lucide:tags',
        'mode' : false
    },
    {
        'id' : 4,
        'name' : 'Lokasi Strategis',
        'icon' : 'lucide:map-pin',
        'mode' : true
    },
    {
        'id' : 5,
        'name' : 'Fasilitas Penunjang',
        'icon' : 'lucide:smile',
        'mode' : false
    },
    {
        'id' : 6,
        'name' : 'Grande Living Room',
        'icon' : 'lucide:bed-double',
        'mode' : true
    }
])

const locations = ref([
    {
        'id' : 1,
        'name' : 'dari Alun-alun Jombang',
        'distance' : '15 menit',
        'mode' : false
    },
    {
        'id' : 2,
        'name' : 'dari Stasiun terdekat',
        'distance' : '8 menit',
        'mode' : false
    },
    {
        'id' : 3,
        'name' : 'dari Rumah Sakit terdekat',
        'distance' : '9 menit',
        'mode' : false
    },
    {
        'id' : 4,
        'name' : 'dari Pasar Taman Mojoagung',
        'distance' : '9 menit',
        'mode' : false
    },
    {
        'id' : 5,
        'name' : 'dari Puskesmas terdekat',
        'distance' : '5 menit',
        'mode' : false
    },
    {
        'id' : 6,
        'name' : 'dari Fasilitas Pendidikan terdekat',
        'distance' : '5 menit',
        'mode' : false
    },
])

const contacts = ref([
    {
        'id' : 1,
        'description' : 'Ds. Sambirejo, Kec. Jogoroto, Jombang',
        'icon' : 'lucide:home',
        'mode' : false
    },
    {
        'id' : 2,
        'description' : '0822 - 3137 - 2191',
        'icon' : 'lucide:phone-call',
        'mode' : false
    },
    {
        'id' : 3,
        'description' : 'griyasambirejoindah@gmail.com',
        'icon' : 'lucide:mail',
        'mode' : false
    },
    {
        'id' : 4,
        'description' : 'www.griyasambirejoindah.com',
        'icon' : 'lucide:globe',
        'mode' : false
    },
    {
        'id' : 1,
        'description' : '@griya_sambirejo',
        'icon' : 'lucide:instagram',
        'mode' : false
    },
])

</script>

<style scoped>

</style>