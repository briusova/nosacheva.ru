<template>
    <div class="min-h-dvh" un-cloak>
        <div class="sticky top-0 z-50 pa-4 border-b bg-neutral-50 border-slate-200 opacity-0 md:hover:opacity-100 transition-opacity duration-1000"
            :class="{ 'opacity-100': !ready }" ref="pageHeader">
            <el-page-header icon="" :content="pages[$route.name].title">
                <template #breadcrumb>
                    <el-breadcrumb separator="/">
                        <el-breadcrumb-item v-for="item in pages[$route.name].branch.slice(1)" :to="item.to">
                            {{ item.name }}
                        </el-breadcrumb-item>
                    </el-breadcrumb>
                </template>
                <template #title>
                    <router-link to="/" class="whitespace-nowrap flex items-center max-sm:hidden">
                        <el-avatar size="small"><i :class="the.i"></i></el-avatar>
                    </router-link>
                </template>
                <template #extra>
                    <el-button circle @click="drawer = true">
                        <icon icon="mdi:menu" class="size-5"></icon>
                    </el-button>
                </template>
            </el-page-header>
        </div>
        <div id="content"><router-view></router-view></div>
    </div>
    <div class="mt-10 bg-[#474350] bg-[url(images/st1.png)]" id="bottom" un-cloak>
        <div class="ui container pt-7 pb-1">
            <div class="ui horizontal basic segments">
                <div class="ui basic segment" style="width: 50%;">
                    <p><i class="envelope large icon" style="color: lightskyblue;"><!-- icon--></i></p>
                    <p style="color: #dcdcdc;">Вопросы об использовании или приобретении материалов, Ваши предложения,
                        отзывы, а также другие вопросы присылайте на почту:<br><a href="mailto:briusova@gmail.com"
                            style="text-decoration: none; color: lightskyblue;">briusova@gmail.com</a><br><br>Согласие
                        на
                        обработку данных не требуется, ничего не обрабатывается.</p>
                </div>
                <div class="ui basic segment" style="width: 50%;">
                    <p><i class="info circle large icon" style="color: lightskyblue;"><!-- icon--></i></p>
                    <p style="color: #dcdcdc;">&copy; Все права защищены. Копирование материала возможно только с
                        согласия
                        владельца сайта. Использование любой медицинской информации в личных целях требует
                        дополнительной
                        консультации врача. Все данные, опубликованные на сайте приведены исключительно для
                        ознакомления,
                        носят информационный характер. На сайте отсутствуют cookies, аналитика и формы сбора данных.</p>
                </div>
            </div>
            <p>&nbsp;</p>
            <p style="font-size: 10pt; text-align: center; color: #dcdcdc; padding-bottom: 5px;"><a
                    class="hvr-wobble-skew" href="https://vuebro.ru/" rel="noopener"
                    style="color: #dcdcdc; font-family: Arsenal, sans-serif; font-size: 12px;"
                    title="VueBro удобный инструмент для управления сайтом" target="_blank">VueBro удобный инструмент для управления сайтом</a>
            </p>
        </div>
    </div>
    <div id="drawer" un-cloak>
        <el-drawer v-model="drawer" :title="the.header" class="w-full sm:w-96" size="">
            <el-menu :router="true">
                <template v-for="({ name, $children, icon, id }, index) in the.$children[0].$children">
                    <el-sub-menu :index="index" v-if="$children.length">
                        <template #title>
                            <icon :icon="icon" class="icon-box"></icon><span>{{ name }}</span>
                        </template>
                        <el-menu-item v-for="(child, index2) in $children" :route="{ name: child.id }" :index="index2">
                            <icon :icon="child.icon" class="icon-box"></icon><span>{{ child.name }}</span>
                        </el-menu-item>
                    </el-sub-menu>
                    <el-menu-item :index="index" :route="{ name: id }" v-else>
                        <icon :icon="icon" class="icon-box"></icon><span>{{ name }}</span>
                    </el-menu-item>
                </template>
            </el-menu>
        </el-drawer>
    </div>
    <el-backtop></el-backtop>
</template>
<script setup>
import { useRoute } from "vue-router";
import { ref, inject, useTemplateRef, onMounted, watch, getCurrentInstance } from "vue";
import { get, set } from "@vueuse/core";
import ElementPlus from "element-plus";
import { Icon } from "@iconify/vue";


const { appContext: { app } } = getCurrentInstance();
app.component("Icon", Icon);
app.use(ElementPlus);
const { id } = defineProps(["id"]),
    pages = inject("pages"),
    the = pages[id],
    ready = ref(true),
    pageHeaderRef = useTemplateRef("pageHeader"),
    drawer = ref(false),
    route = useRoute();
onMounted(() => {
    let timeoutID;
    const scroll = () => {
        set(ready, false);
        if (timeoutID) clearTimeout(timeoutID);
        if (window.scrollY > get(pageHeaderRef, "offsetHeight")) timeoutID = setTimeout(() => {
            set(ready, true);
        }, 2000);
    };
    document.addEventListener("scroll", scroll);
    scroll();
});
watch(() => route.name, () => { drawer.value = false });
</script>
<style>
@import "./node_modules/animate.css/animate.min.css";
@import "./node_modules/hover.css/css/hover-min.css";
@import "./node_modules/element-plus/dist/index.css";
@import "./node_modules/fomantic-ui-css/semantic.min.css";

.el-drawer .el-menu {
    border-right: none;
}

#drawer :deep(.el-drawer__body) {
    padding: 0;
}

.icon-box {
    margin-right: 1rem;
    width: 2rem;
    height: 2rem;
}

hr {
    border: none;
    color: red;
    background-color: DimGray;
    height: 1px;
}

#content {
    font-family: Arsenal, sans-serif;
    line-height: 160%;
    font-size: 18px;
}

#bottom {
    font-family: Arsenal, sans-serif;
}

H1 {
    font-family: Arsenal, sans-serif;
}

H2 {
    font-family: Arsenal, sans-serif;
}

H3 {
    font-family: Arsenal, sans-serif;
}

H4 {
    font-family: Arsenal, sans-serif;
}
</style>