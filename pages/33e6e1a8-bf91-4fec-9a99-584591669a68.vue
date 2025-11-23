<template>
    <div ref="jarallaxRef" class="ui basic vertical fitted segment jarallax mceNonEditable min-h-[75vh]"
        :style="`background-image:url(${url})`">
        <div class="ui active light dimmer" style="position: relative; min-height: 75vh; height: 100%;">
            <div class="ui container">
                <div class="ui huge inverted header right aligned"
                    style="font-family: Arsenal, sans-serif; line-height: 180%;">НОСАЧЕВА<br>Наталия Григорьевна<span
                        class="sub header">1945 – 2021</span></div>
            </div>
        </div>
    </div>
    <div class="ui container">
        <p>&nbsp;</p>
        <h1 style="text-align: center;"><span style="color: rgb(186, 55, 42);">Этот сайт о жизни великой женщины -
                враче,
                целителе и педагоге Наталии Григорьевне Носачевой от её учеников.</span></h1>
        <p>🔸врач высшей категории, психолог, автор книги "Вспомни о своём ясновидении", создатель Школы
            саморегуляции<br>🔸кавалер ордена I степени "За профессиональную честь, достоинство и почётную деловую
            репутацию"<br>🔸награждена Международной золотой медалью ООН "За заслуги перед обществом"</p>

        <p style="text-align: justify; margin-top: 30px;">Дорогие друзья и ученики Школы!

            Школа закрыта, но наследие Наталии Григорьевны живёт.

            На канале <a href="https://t.me/SchoolSelfregulation" rel="noopener"
                target="_blank"><b>ВзаимоДействие</b></a> мы делимся воспоминаниями, проводим встречи и практические
            сессии с разбором
            реальных кейсов, а также отвечаем на ваши вопросы, помогая каждому найти свой путь к гармонии и здоровью.
        </p>
        
        <p style="text-align: center;"><a href="https://t.me/SchoolSelfregulation" rel="noopener"
                target="_blank"><button class="ui large pink basic button"
                    style="font-family: Arsenal, sans-serif; border-radius: 20px;">TELEGRAM-КАНАЛ</button></a></p>

<p style="text-align: justify;">Все материалы Школы — уникальные методики сохранения энергии, очищения организма
            и восстановления эмоционального баланса — надёжно сохранены учениками. Мы используем то, чему нас научила
            Наталия Григорьевна, чтобы живое знание об Учителе и её уникальном подходе передавалось дальше. Сегодня, в
            эпоху хронического стресса
            и цифровой перегрузки, методики Наталии Григорьевны актуальны как никогда.</p>


        <p>&nbsp;</p>

        <div class="ui three column centered stretched padded grid mceNonEditable stackable doubling">
            <div v-for="(child, i) in page.$children" class="column animate__animated"
                :class="{ animate__flipInY: animate[i], invisible: !animate[i], }"
                v-intersection-observer="([{ isIntersecting }]) => { animate[i] = isIntersecting }">
                <div class="ui fluid raised link card">
                    <div class="ui image" ref="cards">
                        <div class="ui inverted dimmer"><router-link :to="child.to"
                                class="ui circular inverted secondary icon button"><i class="icon !h-3"
                                    :class="child.i"></i></router-link></div>
                        <img class="ui image" loading="eager" :src="child.images[0]?.url">
                    </div>
                    <div class="content"><router-link class="ui header hvr-icon-wobble-vertical"
                            style="font-family: Arsenal, sans-serif;" :to="child.to"><i
                                style="vertical-align:top;padding-top:0.3em;" class="hvr-icon icon user md"></i><span
                                class="ui content">{{ child.title }}<span class="sub header">{{
                                    child.description }}</span></span></router-link></div>
                </div>
            </div>
        </div>
        <p>&nbsp;</p>
    </div>
</template>

<script setup>
import { useScriptTag } from "@vueuse/core";
import { inject, onMounted, useTemplateRef, ref, onUnmounted } from "vue";
import { jarallax } from "jarallax";
import { vIntersectionObserver } from "@vueuse/components";

const { id } = defineProps(["id"]),
    page = inject("pages")[id],
    [{ url }] = page.images,
    jarallaxRef = useTemplateRef("jarallaxRef"),
    cardRefs = useTemplateRef("cards"),
    animate = ref([]),
    { load: loadJQuery, unload: unloadJQuery } = useScriptTag("./node_modules/jquery/dist/jquery.min.js", () => { }, { manual: true }),
    { load: loadFomantic, unload: unloadFomantic } = useScriptTag("./node_modules/fomantic-ui-css/semantic.min.js", () => { }, { manual: true });

onMounted(async () => {
    jarallax(jarallaxRef.value, {});
    await loadJQuery();
    await loadFomantic();
    $(cardRefs.value).dimmer({
        transition: "fade up",
        on: "hover",
    });
});

onUnmounted(async () => {
    await unloadFomantic();
    await unloadJQuery();
});
</script>
