<template>
    <div class="relative overflow-hidden">
        <Navbar />
        <div v-motion-slide-visible-once-bottom class="relative mt-24 lg:mt-32  px-4 lg:px-32 py-10">
            <div class="relative z-30 grid grid-cols-6 rounded-xl items-start gap-6 ">
                <div class="relative flex gap-4 justify-between items-center col-span-6 lg:col-span-3 rounded-xl">
                    <video class="rounded-3xl shadow-md" autoplay loop muted>
                        <source src="/bumper.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="col-span-6 lg:col-span-3 flex flex-col gap-3 lg:gap-4 lg:pl-6">
                    <h3 class="font-oswald text-3xl lg:text-5xl tracking-tight text-gsi-darkblue"><span class="text-gsi-gold">Tentang</span> Griya Sambirejo Indah</h3>
                    <p class="indent-8 text-sm lg:text-base text-justify">Griya Sambirejo Indah adalah kawasan perumahan yang dikembangkan oleh PT. Berkah Karya Agung dengan mengusung konsep hunian modern minimalis yang terjangkau. Berlokasi strategis di Desa Sambirejo, Kec. Jogoroto, Kab. Jombang, dekat dengan berbagai fasilitas umum & Jalan utama Nasional serta kurang dari 15 menit dari pusat Jombang.</p>
                    <p class="indent-8 text-sm lg:text-base text-justify">
                        Griya Sambirejo Indah menjadi pilihan tepat bagi anda yang menginginkan hunian dengan suasana nyaman, jauh dari kebisingan, namun dekat dengan berbagai fasilitas publik penunjang kebutuhan anda. Segera dapatkan hunian impian anda bersama kami Griya Sambirejo Indah.
                    </p>
                </div>
            </div>
            <p class="absolute py-10 -right-56 opacity-20 md:opacity-50 top-10">
                <Icon name="PatternThree" class="text-[28rem] rotate-180"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
            <p class="absolute py-10 -left-56 opacity-20 md:opacity-50 bottom-0">
                <Icon name="PatternThree" class="text-[28rem] rotate-180"/>
                <!-- <nuxt-img src="/img/circle01.svg" loading="lazy" sizes="sm:50vw" class="object-cover  object-center h-96 w-full"/> -->
            </p>
        </div>
        <ContactSection/>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>