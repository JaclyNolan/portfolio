<template>
    <div class="container" id="projects-sheet">
        <div id="projects-content">
            <h3>
                Portfolio
            </h3>
            <p>
                Each project is a unique piece of development 🧩
            </p>
            <div id="projects-grid">
                <v-sheet class="project-showcase" elevation="3" rounded="lg">
                    <v-sheet class="project-windows-container">
                        <v-window class="project-windows" v-model="portfolioWindow" show-arrows="hover">
                            <v-window-item v-for="(image, index) in portolioWindowImages" :key="index">
                                <v-img class="project-image bg-gray" :src="image.path" :aspect-ratio="16 / 9" />
                            </v-window-item>
                        </v-window>
                    </v-sheet>
                    <div class="project-description">
                        <h3>Portfolio <span class="project-date">(January 2024)</span></h3>
                        <p>A viewable portfolio to display my personal projects as well as real projects. The website's
                            design was based on another React portfolio developer. It can adapt to any screensize while
                            still remain stylish throughout. It is built on Vue and SCSS</p>
                        <div class="stack">
                            <v-sheet class="stack-item" elevation="3">Vue</v-sheet>
                            <v-sheet class="stack-item" elevation="3">SCSS</v-sheet>
                        </div>
                        <div class="links">
                            <v-hover v-slot:default="{ isHovering, props }">
                                <v-btn class="link-btn" v-bind="props" append-icon="mdi-github" variant="Text" :color="isHovering ? '#147efb'
                                    : '#2d2e32'">Code</v-btn>
                            </v-hover>
                            <v-hover v-slot:default="{ isHovering, props }">
                                <v-btn class="link-btn" v-bind="props" append-icon="mdi-palette" variant="Text" :color="isHovering ? '#147efb'
                                    : '#2d2e32'">Design</v-btn>
                            </v-hover>
                        </div>
                    </div>
                </v-sheet>
            </div>
        </div>
    </div>
</template>
<script>
// import image from "@/assets/youtube-example.png";
export default {
    data() {
        return {
            portfolioWindow: true,
            portolioWindowImages: [
                { path: require('@/assets/portfolio_example_1.png') },
                { path: require('@/assets/portfolio_example_2.png') },
            ],
        }
    },
}
</script>
<style lang="scss">
#projects-sheet {
    display: grid;
    grid-template-columns: 1fr;
    text-align: center;
    align-items: center;
    justify-content: center;
}

#projects-content {
    display: grid;
    grid-template-columns: 1fr;
    padding: 0 0.5rem;
}

#projects-content>h3 {
    font-family: Poppins, sans-serif;
    font-size: var(--fs-500);
    color: #147efb;
    font-weight: 700;
    text-transform: uppercase;
}

#projects-content>p {
    font-family: Poppins, sans-serif;
    font-size: var(--fs-600);
    color: #2d2e32;
    font-weight: 700;
    margin-top: 0.5rem;
}

.project-showcase {
    display: grid;
    grid-template-columns: 1fr;
    color: white;
    margin: 3rem 0.5rem 0 0.5rem;
    padding: 0rem;
}

.project-windows-container {
    padding: 1rem;
}

.project-image {
    width: 100%;
}

.project-description {
    padding: 0 1rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin: 1rem 0;
}

.project-description h3 {
    color: #2d2e32;
    font-size: var(--fs-600);
    font-weight: 700;
    font-family: Poppins, sans-serif;
    text-transform: capitalize;
}

.project-description h3>span {
    color: hsla(0, 5%, 8%, .773);
    font-size: var(--fs-500);
    text-transform: capitalize;
    font-family: Poppins, sans-serif;
}

.project-description p {
    color: #767676;
    font-size: var(--fs-400);
    font-weight: 500;
    font-family: Mulish, sans-serif;
}

.stack {
    display: flex;
    gap: 1rem;
    justify-content: center;
}

.stack-item {
    display: block;
    padding: 0.5rem;
    font-family: Mulish, sans-serif;
    font-size: var(--fs-500);
    font-weight: 600;
}

.links {
    margin-top: 1rem;
}

.link-btn {
    font-size: var(--fs-400);
}
</style>