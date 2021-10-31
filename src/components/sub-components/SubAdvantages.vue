<template>
    <div class="main-list">
        <img :src="require(`../../assets/images/svg/${ad.icon}`)" width="45px" height="45px"/>
        <h3>{{ ad.title }}</h3>
        <p>{{ ad.text }}</p>
    </div>
</template>

<script>
    export default {
        name: 'SubAdvantages',
        props: {
            ad: Object,
        },
        data() {
            return {}
        },
    }
</script>

<style lang="scss" scoped>

.main-list {
    max-width: 280px;
    display: flex;
    flex-direction: column;
    align-items: center;

    img {
        margin-bottom: 22px;
        padding: 0;
    }

    h3 {
        font-weight: bold;
        font-size: 18px;
        line-height: 18px;
        text-align: center;
        color: #1D1D20;
        padding: 0;
        margin-bottom: 12px;
        margin-top: 0;
    }

    p {
        max-width: 280px;
        margin: 0;
        padding: 0;
        font-size: 15px;
        line-height: 20px;
        text-align: center;
        color: #A6A6A6;
    }
}
</style>