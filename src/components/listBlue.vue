<script>
export default {
    components: {
        name: "listBlue",
    },
    data() {
        return {
            items: [
                {
                    id: 1,
                    image: 'buy-comics-digital-comics.png',
                    title: 'DIGITAL COMICS',

                },
                {
                    id: 2,
                    image: 'buy-comics-merchandise.png',
                    title: 'DC MERCHANDISE',

                },
                {
                    id: 3,
                    image: 'buy-comics-subscriptions.png',
                    title: 'SUBSCRIPTION',

                },
                {
                    id: 4,
                    image: 'buy-comics-shop-locator.png',
                    title: 'COMICS SHOP LOCATOR',

                },
                {
                    id: 5,
                    image: 'buy-dc-power-visa.svg',
                    title: 'DC POWER VISA',

                },
            ],
        };
    },
};
</script>

<template>
    <div class="listblu">
        <ul>
            <li v-for="item in items" :key="item.id" class="listitem">
                <img :src="item.image" alt="Thumbnail" class="itemimage" />
                <div class="itemdetails">
                    <h3>{{ item.title }}</h3>
                </div>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/_variables' as *;
@use '../styles/partials/_mixins.scss' as *;

.listblu {
    background-color: rgba(2, 130, 249, 255);
    display: flex;




    h3 {
        font-size: 12px;
        color: white;
    }


    .listitem {
        display: flex;
        align-items: center;
        justify-content: space-around;
        margin-bottom: 20px;
        float: left;
        padding: 30px;

    }

    .itemimage {
        max-width: 50px;
        max-height: 50px;
        margin-right: 20px;
    }



}
</style>