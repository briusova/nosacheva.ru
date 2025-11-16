<template>
    <div ref="jarallaxRef" class="ui basic vertical fitted segment jarallax mceNonEditable  min-h-[60vh]"
        :style="`background-image:url(${url})`">
        <div class="ui active light dimmer">
            <div class="content"><a class="ui header hvr-icon-wobble-vertical massive inverted icon"
                    style="font-family: Arsenal, sans-serif;"><i class="hvr-icon !h-28 icon mx-auto"
                        :class="page.i"></i><span class="ui">{{ page.title }}<span class="sub header">{{
                            page.description
                            }}</span></span></a></div>
        </div>
    </div>
    <p>&nbsp;</p>
    <div class="ui container">
        <p style="text-align: justify;">7 февраля 2009 года на "Конгрессе элиты народной альтернативной медицины" в
            Москве
            сделаны 2 снимка ауры Наталии Григорьевны Носачевой. На рисунке №1 показана повседневная аура, а на рисунке
            №2
            показана аура, сделанная&nbsp;через&nbsp;2 минуты.&nbsp;На рисунке №2 показан "рабочий" момент, т.е
            концентрация
            через мыслеформы.</p>
        <p style="text-align: justify;">При "рабочем" моменте видно, что работает в основном ДУХ (так называемое
            Будхуальное
            (розовое тонкое) тело). РАЗУМ и ТЕЛО имеют мизерные доли присутствия работы.<strong><br></strong></p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img1" :src="src" :preview-src-list="srcList1"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <p style="text-align: justify;">Разъяснения к стрелке №1 на рисунках №1 и №2:</p>
        <p style="text-align: justify;">✦ синий цвет - мозг<br>✦ зеленый цвет - тело<br>✦ голубой цвет - дух</p>
        <p style="text-align: justify;">Разъяснения к стрелке №2 на рисунках №1 и №2:</p>
        <p style="text-align: justify;">на рис. №1 показан обычный размер ауры Н.Г.Носачевой, на рис. №2 - размер ауры
            при
            концентрации (работе). Видно, что поле (аура) уменьшается.</p>
        <p style="text-align: justify;"><strong>Именно по этой причине не подготовленным людям не рекомендуется
                заниматься
                подобной практикой. Если человек не умеет восстанавливать силы и ставить защиту от негатиных
                воздействий,
                при работе он может принять на себя чужую негативную энергию, информацию, вибрации.</strong></p>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>Способности Наталии Григорьевны помогли этой семье стать счастливыми родителями</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img2" :src="src" :preview-src-list="srcList2"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>Доктор Игнат Игнатов (Болгария), Наталия Носачева и участники VII Международной конференции"Человек и
            природа",
            2007 год</p>
        <div class="ui centered small images">
            <el-image class="ui rounded image" src="images/IMG_0470-2.jpg" :preview-src-list="['images/IMG_0470.jpg']"
                fit="cover" alt="Носачева Наталия и Игнат Игнатов" title="Носачева Наталия и Игнат Игнатов"
                preview-teleported></el-image>
        </div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>VII Международный Форум"ИНТЕГРАТИВНАЯ МЕДИЦИНА 2012"</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img3" :src="src" :preview-src-list="srcList3"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>VIII съезд Элиты специалистов традиционной народной медицины и целительства 2012 года</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img4" :src="src" :preview-src-list="srcList4"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>На творческой встрече в честь 20-летия Российской Ассоциации Целителей (декабрь 2011)</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img5" :src="src" :preview-src-list="srcList5"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>Выступление в Центральном Доме работников искусств</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img6" :src="src" :preview-src-list="srcList6"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>Хельсинский Европейский форум, международная конференция "Здравоохранение XXI века: фундаментальные ценности,
            новые технологии, подходы"</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img7" :src="src" :preview-src-list="srcList7"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>&nbsp;</p>
        <p>Наталия Григорьевна с пациентами</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img8" :src="src" :preview-src-list="srcList8"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <div class="ui divider">&nbsp;</div>
        <p>"Человек и природа"</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img9" :src="src" :preview-src-list="srcList9"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <p>&nbsp;</p>


<p>Будни Школы саморегуляции</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img10" :src="src" :preview-src-list="srcList10"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <p>&nbsp;</p>



        <p>Отзывы о Школе саморегуляции и после приёмов у Наталии Носачевой</p>
        <p>Отзывы размещались на сайте Школы https://natalie-school.ru. Сейчас сайт Школы закрыт.</p>
        <div class="ui centered small images"><el-image class="ui rounded image"
                v-for="({ src, title, alt }, index) in img11" :src="src" :preview-src-list="srcList11"
                :initial-index="index" fit="cover" :alt="alt" :title="title" preview-teleported></el-image></div>
        <p>&nbsp;</p>

        <router-link :to="page.parent.to" class="ui labeled icon fluid red button"
            style="font-family: Arsenal, sans-serif;"><i class="left arrow icon"></i>на
            главную</router-link>






            
    </div>




</template>

<script setup>
import { inject, useTemplateRef, onMounted } from "vue";
import { jarallax } from "jarallax";

const { id } = defineProps(["id"]),
    page = inject("pages")[id],
    [{ url }] = page.images,
    jarallaxRef = useTemplateRef("jarallaxRef"),
    img1 = [
        { src1: "files/foto/aura1big.jpg", title: "Носачева Наталия", src: "files/foto/aura1big.jpg", alt: "Носачева Наталия" },
        { src1: "files/foto/aura2big.jpg", title: "Носачева Наталия", src: "files/foto/aura2big.jpg", alt: "Носачева Наталия" },
    ],
    srcList1 = img1.map(({ src1 }) => src1),
    img2 = [
        {
            src1: "files/foto/family/family1.jpg",
            title: "Носачева Наталия",
            src: "files/foto/family/family1_m.jpg",
            alt: "Носачева Наталия"
        },
        {
            src1: "files/foto/family/family2.jpg",
            title: "Носачева Наталия",
            src: "files/foto/family/family2_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/family/family3.jpg",
            title: "Носачева Наталия",
            src: "files/foto/family/family3_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/family/family4.jpg",
            title: "Носачева Наталия",
            src: "files/foto/family/family4_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/family/family5.jpg",
            title: "Носачева Наталия",
            src: "files/foto/family/family5_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/family/family6.jpg",
            title: "Носачева Наталия",
            src: "files/foto/family/family6_m.jpg",
            alt: "Носачева Наталия"
        },
    ],
    srcList2 = img2.map(({ src1 }) => src1),
    img3 = [
        {
            src1: "files/foto/forum2012/forum1.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum1_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum2.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum2_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum3.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum3_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum4.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum4_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum5.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum5_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum6.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum6_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum7.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum7_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum8.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum8_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum9.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum9_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum10.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum10_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum11.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum11_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum12.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum12_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum13.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum13_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum14.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum14_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum15.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum15_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum16.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum16_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum17.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum17_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum18.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum18_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum19.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum19_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum20.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum20_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum21.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum21_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum22.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum22_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum23.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum23_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum24.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum24_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum25.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum25_m.jpg",
            alt: "Носачева Наталия"
        }, {
            src1: "files/foto/forum2012/forum26.jpg",
            title: "Носачева Наталия",
            src: "files/foto/forum2012/forum26_m.jpg",
            alt: "Носачева Наталия"
        },],
    srcList3 = img3.map(({ src1 }) => src1),
    img4 = [{ src1: "files/foto/8elit.jpg", title: "Носачева Наталия", src: "files/foto/8elit_m.jpg", alt: "Носачева Наталия" }, { src1: "images/ja8ZbExuNuA.jpg", title: "Носачева Наталия", src: "images/ja8ZbExuNuA-2.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/8elit2.jpg", title: "Носачева Наталия", src: "files/foto/8elit2_m.jpg", alt: "Носачева Наталия" },],
    srcList4 = img4.map(({ src1 }) => src1),
    img5 = [{ src1: "files/foto/vstr.jpg", title: "Носачева Наталия", src: "files/foto/vstr_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/vstr2.jpg", title: "Носачева Наталия", src: "files/foto/vstr2_m.jpg", alt: "Носачева Наталия" },],
    srcList5 = img5.map(({ src1 }) => src1),
    img6 = [{ src1: "files/foto/centr_dom/cd.jpg", title: "Носачева Наталия", src: "files/foto/centr_dom/cd_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/centr_dom/cd2.jpg", title: "Носачева Наталия", src: "files/foto/centr_dom/cd2_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/centr_dom/cd3.jpg", title: "Носачева Наталия", src: "files/foto/centr_dom/cd3_m.jpg", alt: "Носачева Наталия" },],
    srcList6 = img6.map(({ src1 }) => src1),
    img7 = [{ src1: "files/foto/helsinky/1.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/1m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/2.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/2m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/4.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/4m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/5.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/5m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/6.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/6m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/7.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/7m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/8.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/8m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/9.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/9m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/10.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/10m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/11.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/11m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/helsinky/12.jpg", title: "Носачева Наталия", src: "files/foto/helsinky/12m.jpg", alt: "Носачева Наталия" },],
    srcList7 = img7.map(({ src1 }) => src1),
    img8 = [{ src1: "files/foto/pacient/p1.jpg", title: "Носачева Наталия", src: "files/foto/pacient/p1_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/pacient/p2.jpg", title: "Носачева Наталия", src: "files/foto/pacient/p2_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/pacient/p3.jpg", title: "Носачева Наталия", src: "files/foto/pacient/p3_m.jpg", alt: "Носачева Наталия" },],
    srcList8 = img8.map(({ src1 }) => src1),
    img9 = [{ src1: "files/foto/chelov/s1.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s1_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s2.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s2_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s3.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s3_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s4.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s4_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s5.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s5_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s6.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s6_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s7.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s7_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s8.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s8_m.jpg", alt: "Носачева Наталия" }, { src1: "files/foto/chelov/s9.jpg", title: "Носачева Наталия", src: "files/foto/chelov/s9_m.jpg", alt: "Носачева Наталия" },],
    srcList9 = img9.map(({ src1 }) => src1);

const img10 = [
    {
        src1: "images2/1.jpg",
        title: "Носачева Наталия",
        src: "images2/1m.jpg",
        alt: "Носачева Наталия",
    },
    {
        src1: "images2/2.jpg",
        title: "Носачева Наталия",
        src: "images2/2m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/3.jpg",
        title: "Носачева Наталия",
        src: "images2/3m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/4.jpg",
        title: "Носачева Наталия",
        src: "images2/4m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/5.jpg",
        title: "Носачева Наталия",
        src: "images2/5m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/6.jpg",
        title: "Носачева Наталия",
        src: "images2/6m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/7.jpg",
        title: "Носачева Наталия",
        src: "images2/7m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/8.jpg",
        title: "Носачева Наталия",
        src: "images2/8m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/9.jpg",
        title: "Носачева Наталия",
        src: "images2/9m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/10.jpg",
        title: "Носачева Наталия",
        src: "images2/10m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/11.jpg",
        title: "Носачева Наталия",
        src: "images2/11m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/12.jpg",
        title: "Носачева Наталия",
        src: "images2/12m.jpg",
        alt: "Носачева Наталия",
    },
 {
        src1: "images2/13.jpg",
        title: "Носачева Наталия",
        src: "images2/13m.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/14.jpg",
        title: "Носачева Наталия",
        src: "images2/14m.jpg",
        alt: "Носачева Наталия",
    },
];

const srcList10 = img10.map(({ src1 }) => src1);

const img11 = [
    {
        src1: "images2/otzuv1.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuv1.jpg",
        alt: "Носачева Наталия",
    },
    {
        src1: "images2/otzuv2.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuv2.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuv3.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuv3.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuv4.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuv4.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuv5.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuv5.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw1.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw1.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw2.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw2.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw3.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw3.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw4.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw4.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw5.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw5.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw6.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw6.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw7.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw7.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw8.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw8.jpg",
        alt: "Носачева Наталия",
    },
        {
        src1: "images2/otzuw9.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw9.jpg",
        alt: "Носачева Наталия",
    },

            {
        src1: "images2/otzuw10.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw10.jpg",
        alt: "Носачева Наталия",
    },
            {
        src1: "images2/otzuw11.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw11.jpg",
        alt: "Носачева Наталия",
    },
            {
        src1: "images2/otzuw12.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw12.jpg",
        alt: "Носачева Наталия",
    },
            {
        src1: "images2/otzuw13.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw13.jpg",
        alt: "Носачева Наталия",
    },
            {
        src1: "images2/otzuw14.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw14.jpg",
        alt: "Носачева Наталия",
    },
            {
        src1: "images2/otzuw15.jpg",
        title: "Носачева Наталия",
        src: "images2/otzuw15.jpg",
        alt: "Носачева Наталия",
    },
];

const srcList11 = img11.map(({ src1 }) => src1);


onMounted(() => { jarallax(jarallaxRef.value, {}) });
</script>