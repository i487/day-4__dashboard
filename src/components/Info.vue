<template>
    <section class="info">
        <div class="info__card" v-for="(item, index) in information" :key="index">
            <span class="info__card-icon" v-html="item.icon"></span>
            <div class="info__card-context">
                <h2 class="info__card-title"> {{ item.title }} </h2>
                <p class="info__card-index"> {{ item.indicator }} </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Info",
    props: ["information"]
}
</script>

<style lang="scss">
.info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 32px;
    &__card {
        display: flex;
        align-items: center;
        gap: 24px;
        background: #FFFFFF;
        box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
        border-radius: 8px;
        padding: 20px 24px;
        width: 255px;
        &-title {
            font-weight: bold;
            font-size: 14px;
            line-height: 20px;
            color: #25282B;
        }
        &-index {
            font-size: 18px;
            line-height: 24px;
            color: #336CFB;
        }
    }
}
</style>