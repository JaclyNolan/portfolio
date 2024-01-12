<template>
    <v-sheet id="home-sheet">
        <v-sheet id="hero-card">
            <img id="hero-avatar" :src="require('@/assets/avatar.jpg')" alt="Jack_Ánh" />
            <h1>Front-End React Developer <img id="hero-emoji" :src="require('@/assets/waving_hand.png')" alt="waving_hand">
            </h1>
            <p>
                Hi, I'm Jack Ánh. A passionate Front-end React/Vue Developer based in Hanoi, Vietnam.
            </p>
            <span id="hero-social">
                <v-icon icon="mdi-linkedin" size="30"></v-icon>
                <v-icon icon="mdi-github" size="30"></v-icon>
            </span>
        </v-sheet>
        <v-sheet id="skills">
                <p>Tech Stack</p>
            <div id="logo">
                <ul>
                    <li>
                        <img src="https://skillicons.dev/icons?i=html,css" alt="html,css"/>
                    </li>
                    <li>
                        <img src="https://skillicons.dev/icons?i=js,ts" alt="javascript,typescript"/>
                    </li>
                    <li>
                        <img src="https://skillicons.dev/icons?i=react,scss" alt="react,scss"/>
                    </li>
                    <li>
                        <img src="https://skillicons.dev/icons?i=vue,laravel" alt="vue,laravel"/>
                    </li>
                </ul>
            </div>
        </v-sheet>
    </v-sheet>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#home-sheet {
    display: flex;
    flex-direction: column;
    height: calc(max(100vh, fit-content));
    background-color: #f9f9f9;
}

#home-sheet * {
    background-color: transparent;
}

#hero-card {
    display: flex;
    flex-direction: column;
    padding: 0 1rem 0 1rem;
    margin: 5rem auto 5rem auto;
    background-color: transparent;
    gap: 1.5rem;
    max-width: 24rem;

}


#hero-card #hero-avatar {
    display: inline-block;
    padding: 0 3rem 0 3rem;
    max-width: 25rem;
    max-height: 25rem;
    object-position: 50% 20%;
    object-fit: cover;
    border-radius: 50%;
}

#hero-card h1 {
    margin-top: 1rem;
    color: #2d2e32;
    display: inline-block;
    text-align: center;
    font-size: var(--fs-xl);
    font-family: Poppins, sans-serif;
    line-height: 1;
}

#hero-card p {
    color: #555;
    display: inline-block;
    text-align: center;
    font-size: var(--fs-400);
    font-family: Mulish, sans-serif;
    font-weight: 500;
    line-height: 1.6;
}

#hero-card #hero-emoji {
    display: inline-block;
    position: relative;
    top: 0.5rem;
    height: var(--fs-xl);
}

#hero-social {
    display: flex;
    gap: 1rem;
    margin: 0 auto 0 auto;
}

#skills {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding: 0 1rem 0 1rem;
}


#skills ul {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 1.5rem;
    list-style: none;
    justify-content: center;
}

#skills p {
    display: flex;
    margin: 0 auto 0 auto;
    font-family: Mulish, sans-serif;
    font-size: var(--fs-500);
    color: #2d2e32;
    font-weight: 600;
    border-bottom: 2px solid rgba(45, 46, 50, .5);
    border-right: none;
    padding-bottom: 0.5rem;
}
</style>