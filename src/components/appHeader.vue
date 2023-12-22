<script>

export default {
    components: {
        name: "appHeader",
    },
    data() {
        return {
            logoSrc: 'url-del-tuo-logo',
            menuItems: [
                {
                    id: 1,
                    title: 'characters',
                    link: '/'
                },
                {
                    id: 2,
                    title: 'comics',
                    link: '/about'
                },
                {
                    id: 3,
                    title: 'movies',
                    link: '/'
                },
                {
                    id: 4,
                    title: 'tv',
                    link: '/about'
                },
                {
                    id: 5,
                    title: 'games',
                    link: '/'
                },
                {
                    id: 6,
                    title: 'collectibles',
                    link: '/about'
                },
                {
                    id: 7,
                    title: 'videos',
                    link: '/'
                },
                {
                    id: 8,
                    title: 'fans',
                    link: '/about'
                },
                {
                    id: 9,
                    title: 'news',
                    link: '/'
                },
                {
                    id: 10,
                    title: 'shop',
                    link: '/about'
                },

            ],
        };
    },
};
</script>

<template>
    <header>
        <div class="logocontainer">
            <img src="/dc-logo.png" alt="dc-logo" />
        </div>
        <div class="menucontainer">
            <ul>
                <li v-for="item in menuItems" :key="item.id">
                    <a :href="item.link" class="menulink">{{ item.title }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/_variables' as *;
@use '../styles/partials/_mixins.scss' as *;

header {

    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-around;
    padding: 10px 20px;


    .logocontainer img {
        max-height: 60px;
    }

    .menucontainer ul {
        list-style: none;
        display: flex;
        margin: 0;
        padding: 0;
    }

    .menucontainer li {
        margin-right: 20px;
    }

    .menucontainer a {
        text-decoration: none;
        color: black;
        font-weight: bold;
    }

    .menucontainer .menulink {
        text-decoration: none;
        color: black;
        font-weight: bold;
        transition: color 0.3s;
        /* Aggiunto per una transizione più fluida del cambio di colore */
    }

    .menucontainer .menulink:hover {
        color: rgba(2, 130, 249, 255);
        /* Cambia il colore del testo al passaggio del mouse */
    }
}
</style>
