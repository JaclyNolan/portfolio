<template>
    <div class="container" id="home-sheet">
        <div id="hero-card">
            <img id="hero-avatar" :src="require('@/assets/avatar.jpg')" alt="Jack_Ánh" />
            <div>
                <h1>Front-End React Developer <img id="hero-emoji" :src="require('@/assets/waving_hand.png')"
                        alt="waving_hand">
                </h1>
                <p>
                    Hi, I'm Jack Ánh. A passionate Front-end React/Vue Developer based in Hanoi, Vietnam.
                </p>
                <span id="hero-social">
                    <a href="https://facebook.com/Jacly123" target="_blank">
                        <v-icon icon="mdi-facebook" size="30"></v-icon>
                    </a>
                    <a href="https://github.com/JaclyNolan" target="_blank">
                        <v-icon icon="mdi-github" size="30"></v-icon>
                    </a>
                </span>
            </div>
        </div>
        <div id="skills">
            <p>Tech Stack</p>
            <div id="logo">
                <ul>
                    <li>
                        <img src="https://skillicons.dev/icons?i=html,css" alt="html,css" />
                    </li>
                    <li>
                        <img src="https://skillicons.dev/icons?i=js,ts" alt="javascript,typescript" />
                    </li>
                    <li>
                        <img src="https://skillicons.dev/icons?i=react,scss" alt="react,scss" />
                    </li>
                    <li>
                        <img src="https://skillicons.dev/icons?i=vue,laravel" alt="vue,laravel" />
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../scss/_breakpoints';

#home-sheet {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    gap: 4rem;

    * {
        background-color: transparent;
    }
}

#hero-card {
    display: flex;
    flex-direction: column;
    padding: 0 1rem 0 1rem;
    background-color: transparent;
    gap: 1.5rem;

    #hero-avatar {
        padding: 0 3rem 0 3rem;
        max-width: 25rem;
        max-height: 25rem;
        object-fit: cover;
        border-radius: 50%;

        @media (min-width: 25rem) {
            align-self: center;
        }
    }

    h1 {
        margin-top: 1rem;
        color: #2d2e32;
        display: inline-block;
        text-align: center;
        font-size: var(--fs-xl);
        font-family: var(--ff-heading);
        line-height: 1;
    }

    p {
        color: #555;
        display: inline-block;
        text-align: center;
        font-size: var(--fs-400);
        font-family: var(--ff-body);
        font-weight: 500;
        line-height: 1.6;
    }

    #hero-emoji {
        display: inline-block;
        position: relative;
        top: 0.5rem;
        height: var(--fs-xl);
    }
}

#hero-social {
    display: flex;
    gap: 1rem;
    margin: 0 auto 0 auto;

    >a {
        text-decoration: none;
        color: inherit;
    }
}

#skills {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding: 0 1rem 0 1rem;

    ul {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 1.5rem;
        list-style: none;
        justify-content: center;
    }

    p {
        display: flex;
        margin: 0 auto 0 auto;
        font-family: var(--ff-body);
        font-size: var(--fs-500);
        color: #2d2e32;
        font-weight: 600;
        border-bottom: 2px solid rgba(45, 46, 50, .5);
        border-right: none;
        padding-bottom: 0.5rem;
    }


}

@include lg {
    #hero-card {
        flex-direction: row-reverse;
    }
}
</style>