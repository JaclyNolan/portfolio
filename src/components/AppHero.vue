<template>
    <v-sheet id="hero-card">
        <img id="hero-avatar" :src="require('@/assets/avatar.jpg')" alt="Jack_Ánh" />
        <h1>Front-End React Developer <img id="hero-emoji" :src="require('@/assets/waving_hand.png')" alt="waving_hand"></h1>
        <p>
            Hi, I'm Jack Ánh. A passionate Front-end React/Vue Developer based in Hanoi, Vietnam. 
        </p>
    </v-sheet>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../scss/_breakpoints';
@import '../scss/_fonts';
$h1FontSize: clamp(2rem, 1rem + 5vw, 4.5rem);
$imgFontSize: calc(#{$h1FontSize});
@debug $imgFontSize;

#hero-card {
    display: flex;
    flex-direction: column;
    padding: 0 1rem 0 1rem;
    background-color: transparent;
    justify-content: center;
    gap: 1.5rem;
    max-width: 24rem;

    @media (min-width: 30rem) {}
}

#hero-card * {
    background-color: transparent;
}

#hero-card #hero-avatar {
    display: flex;
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
    font-size: $h1FontSize;
    font-family: Poppins, sans-serif;
    line-height: 1;
}
#hero-card p {
    color: #555;
    display: inline-block;
    text-align: center;
    font-size: clamp(1rem, 0.5 + 3vw, 3rem);
    font-family: Mulish ,sans-serif;
    font-weight: 500;
    line-height: 1.6;
}

#hero-card #hero-emoji {
    display: inline-block;
    position: relative;
    top: 0.5rem;
    height: $imgFontSize;
}
</style>