<template>
        <div ref="jarallaxRef" class="ui basic vertical fitted segment jarallax mceNonEditable  min-h-[60vh]"
                :style="`background-image:url(${url})`">
                <div class="ui active light dimmer">
                        <div class="content"><a class="ui header hvr-icon-wobble-vertical massive inverted icon"
                                        style="font-family: Arsenal, sans-serif;"><i class="hvr-icon !h-28 icon mx-auto"
                                                :class="page.i"></i><span class="ui">{{ page.title }}<span
                                                        class="sub header">{{
                                                                page.description
                                                        }}</span></span></a></div>
                </div>
        </div>
        <p>&nbsp;</p>
        <div class="ui container">
                <div class="ui dividing header" style="font-family: Arsenal, sans-serif;">НАТАЛИЯ НОСАЧЕВА:
                        <div class="sub header">я живу с надеждой, что мои рекомендации, знания, советы, помогут людям
                                преодолеть недуг
                        </div>
                </div>
                <p style="text-align: justify;">Гоните прочь от себя все негативные мысли и программы.</p>
                <p style="text-align: justify;"><strong>ПОМНИТЕ</strong>:</p>
                <p>🔹 <em>Если вы боитесь, что вас побьют, считайте себя битым.</em></p>
                <p>🔹 <em>Если вы думаете, что не смеете, вы не посмеете никогда.</em></p>
                <p>🔹 <em>Если вам нравится побеждать, но вы думаете, что не сможете победить, вы почти наверняка
                                потерпите
                                поражение.</em></p>
                <p>🔹 <em>Если вы считаете, что проиграли, вы уже проиграли.</em></p>
                <p>🔹 <em>Если вы считаете, что вас оставили позади, это так и есть.</em></p>
                <p style="text-align: justify;">Прежде чем одержать победу, вы должны быть уверены в себе. Это залог
                        свершения всех
                        надежд и стремлений. Включите эти утверждения в свой активный опыт и позитивные изменения не
                        заставят себя
                        ждать.</p>
                <p style="text-align: justify;">Но при этом не стоит ждать, что "манна небесная" будет сыпаться на вас
                        сама собой.
                        Будучи уже довольно известным специалистом, не стесняясь, я училась, не сетовала на неудачи, шла
                        вперёд и была
                        благодарна за всё, что имею.</p>
                <p style="text-align: justify;">Когда-то в юности и молодости я писала стихи. Потом, в силу разных
                        обстоятельств,
                        вдохновение покинуло меня. И я благодарю Высшие силы ещё и за то, что они решили вернуть мне это
                        замечательное
                        ощущение, когда слова сами собой складываются в рифмы и выражают мои чувства.</p>
                <p><strong>Вот одно из моих последних стихотворений:</strong></p>
                <p style="text-align: justify;"><em>Твои глаза сейчас я вижу редко,</em><br><em>По телефону голос
                                иногда.</em><br><em>Судьба ударила молниеносно, метко,</em><br><em>Но, знаю, счастье
                                это. Не
                                беда.</em><br><em>И все твои вдруг стали мне родными,</em><br><em>Живу их помыслами
                                я.</em><br><em>Родная
                                мама, мыслями, привычками своими,</em><br><em>Сестра &ndash; улыбкою, похожей на
                                тебя.</em><br><em>Людей
                                хороших множество на свете.</em><br><em>Спасибо, Господи! Что встретила
                                ещё&hellip;</em><br><em>Так дай им
                                счастья всем. И детям!</em><br><em>Возьми под покровительство своё!</em></p>
                <p style="text-align: justify;"><strong>Хочу пожелать всем очень внимательно относиться к произнесённым
                                словам. И
                                здесь мне хочется привести слова неизвестного автора.</strong></p>
                <p style="text-align: justify;"><em>Небрежное слово - ссору зажжёт,</em><br><em>Жестокое слово - жизнь
                                разобьёт,</em><br><em>Недоброе слово - злобу внушит,</em><br><em>Грубое слово - может
                                убить,</em><br><em>Доброе слово - путь замостит,</em><br><em>Нужное слово - ношу
                                смягчит,</em><br><em>Слово
                                любви - боль облегчит.</em></p>
                <p style="text-align: justify;"><strong>Всем советую копить в своём сердце любовь, убрать из него такие
                                ненужные
                                качества, как обида, злоба, зависть, ревность, и прочие из того же разряда.</strong></p>
                <p style="text-align: justify;"><strong>Я живу с надеждой, что мои рекомендации, знания, советы, помогут
                                людям
                                преодолеть недуг. Самая большая радость для меня - видеть своих пациентов здоровыми. А
                                значит -
                                счастливыми.</strong></p>
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
        jarallaxRef = useTemplateRef("jarallaxRef");

onMounted(() => { jarallax(jarallaxRef.value, {}) });
</script>