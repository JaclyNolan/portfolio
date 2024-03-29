<template>
    <div class="container" id="projects-sheet">
        <div class="projects-content">
            <h3>
                Portfolio
            </h3>
            <p>
                Each project is a unique piece of development 🧩
            </p>
            <div id="projects-grid">
                <v-sheet class="project-showcase" elevation="4" rounded="lg">
                    <v-sheet class="project-windows-container">
                        <v-window class="project-windows elevation-2 rounded-lg" v-model="portfolioWindow"
                            show-arrows="hover">
                            <v-window-item v-for="(image, index) in portolioWindowImages" :key="index">
                                <v-img class="project-image bg-gray" :src="image.path" :aspect-ratio="16 / 9" />
                            </v-window-item>
                        </v-window>
                    </v-sheet>
                    <div class="project-description">
                        <h3>Portfolio <span class="project-date">(January 2024)</span></h3>
                        <p>A viewable portfolio to display my personal projects as well as real projects. The website's
                            design was BASED on Stefan Topalovic's React portfolio. It can adapt to any screensize while
                            still remain stylish throughout. It is built on Vue and SCSS</p>
                        <div class="stack">
                            <v-sheet class="stack-item rounded-sm" elevation="3">Vue</v-sheet>
                            <v-sheet class="stack-item rounded-sm" elevation="3">SCSS</v-sheet>
                        </div>
                        <div class="links">
                            <v-hover v-slot:default="{ isHovering, props }">
                                <a href="https://github.com/JaclyNolan/portfolio" target="_blank">
                                    <v-btn class="link-btn" v-bind="props" append-icon="mdi-github" variant="Text" :color="isHovering ? '#147efb'
                                        : '#2d2e32'">Code</v-btn>
                                </a>
                            </v-hover>
                            <v-hover v-slot:default="{ isHovering, props }">
                                <a href="https://www.stefantopalovic.com/" target="_blank">
                                    <v-btn class="link-btn" v-bind="props" append-icon="mdi-palette" variant="Text" :color="isHovering ? '#147efb'
                                        : '#2d2e32'">Design</v-btn>
                                </a>
                            </v-hover>
                        </div>
                    </div>
                </v-sheet>
                <v-sheet class="project-showcase" elevation="4" rounded="lg">
                    <v-sheet class="project-windows-container">
                        <v-window class="project-windows elevation-2 rounded-lg" v-model="HRWindow" show-arrows="hover">
                            <v-window-item v-for="(image, index) in HRWindowImages" :key="index">
                                <v-img class="project-image bg-gray" :src="image.path" />
                            </v-window-item>
                        </v-window>
                    </v-sheet>
                    <div class="project-description">
                        <h3>Learning Centre Management <span class="project-date">(July 2023)</span></h3>
                        <p>A personal project where you can manage a learning centre database. This project consists of 3
                            roles: Admin, Trainer, Trainee. The features are CRUD, profile information changing, assign
                            many-to-many relationship and edit-then-save quality of life feature. It is built on React and
                            Vanilla CSS</p>
                        <div class="stack">
                            <v-sheet class="stack-item rounded-sm" elevation="3">React</v-sheet>
                            <v-sheet class="stack-item rounded-sm" elevation="3">Vanilla CSS</v-sheet>
                            <v-sheet class="stack-item rounded-sm" elevation="3">Laravel</v-sheet>
                        </div>
                        <div class="links">
                            <v-hover v-slot:default="{ isHovering, props }">
                                <a href="https://github.com/JaclyNolan/HR-Learning-Web-Server" target="_blank">
                                    <v-btn class="link-btn" v-bind="props" append-icon="mdi-github" variant="Text" :color="isHovering ? '#147efb'
                                        : '#2d2e32'">Code</v-btn>
                                </a>
                            </v-hover>
                            <v-hover v-slot:default="{ isHovering, props }">
                                <a href="https://learning-centre-management.vercel.app/" target="_blank">
                                    <v-btn class="link-btn" v-bind="props" append-icon="mdi-television-classic"
                                        variant="Text" :color="isHovering ? '#147efb'
                                            : '#2d2e32'">Live Demo</v-btn>
                                </a>
                            </v-hover>
                        </div>
                    </div>
                </v-sheet>
                <v-sheet class="project-showcase" elevation="4" rounded="lg">
                    <v-sheet class="project-windows-container">
                        <v-window class="project-windows elevation-2 rounded-lg" v-model="UniWindow" show-arrows="hover">
                            <v-window-item v-for="(image, index) in UniWindowImages" :key="index">
                                <v-img class="project-image bg-gray" :src="image.path" />
                            </v-window-item>
                        </v-window>
                    </v-sheet>
                    <div class="project-description">
                        <h3>Uni Academic Portal <span class="project-date">(June 2023)</span></h3>
                        <p>My school's final project. This project consists of 4
                            roles: Admin, Staff, Teacher, Student. The notable features are CRUD, OAuth by Google, a time-based class schedule system, API token, Role and Authorization. It is built on React, Vanilla CSS and Laravel </p>
                        <div class="stack">
                            <v-sheet class="stack-item rounded-sm" elevation="3">React</v-sheet>
                            <v-sheet class="stack-item rounded-sm" elevation="3">Vanilla CSS</v-sheet>
                            <v-sheet class="stack-item rounded-sm" elevation="3">Laravel</v-sheet>
                        </div>
                        <div class="links">
                            <v-hover v-slot:default="{ isHovering, props }">
                                <a href="https://github.com/JaclyNolan/FAP-University-Web-Server" target="_blank">
                                    <v-btn class="link-btn" v-bind="props" append-icon="mdi-github" variant="Text" :color="isHovering ? '#147efb'
                                        : '#2d2e32'">Code</v-btn>
                                </a>
                            </v-hover>
                            <v-hover v-slot:default="{ isHovering, props }">
                                <a href="https://uni-management.vercel.app/" target="_blank">
                                    <v-btn class="link-btn" v-bind="props" append-icon="mdi-television-classic"
                                        variant="Text" :color="isHovering ? '#147efb'
                                            : '#2d2e32'">Live Demo</v-btn>
                                </a>
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
            HRWindow: true,
            HRWindowImages: [
                { path: require('@/assets/HR_example_2.png') },
                { path: require('@/assets/HR_example_1.png') },
                { path: require('@/assets/HR_example_7.png') },
                { path: require('@/assets/HR_example_3.png') },
                { path: require('@/assets/HR_example_4.png') },
                { path: require('@/assets/HR_example_6.png') },
                { path: require('@/assets/HR_example_5.png') },
            ],
            UniWindow: true,
            UniWindowImages: [
                { path: require('@/assets/Uni_example_1.png') },
                { path: require('@/assets/Uni_example_2.png') },
                { path: require('@/assets/Uni_example_3.png') },
                { path: require('@/assets/Uni_example_4.png') },
                { path: require('@/assets/Uni_example_5.png') },
                { path: require('@/assets/Uni_example_6.png') },
                { path: require('@/assets/Uni_example_7.png') },
            ],
        }
    },
}
</script>
<style lang="scss">
@import '../scss/_breakpoints';

.projects-content {
    display: grid;
    grid-template-columns: 1fr;
    padding: 0 0.5rem;

    >h3 {
        font-family: var(--ff-heading);
        font-size: var(--fs-500);
        color: #147efb;
        font-weight: 700;
        text-transform: uppercase;
        text-align: center;
    }

    >p {
        font-family: var(--ff-heading);
        font-size: var(--fs-600);
        color: #2d2e32;
        font-weight: 700;
        margin-top: 0.5rem;
        text-align: center;
    }
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
    text-align: center;

    h3 {
        color: #2d2e32;
        font-size: var(--fs-600);
        font-weight: 700;
        font-family: var(--ff-heading);
        text-transform: capitalize;

        >span {
            color: hsla(0, 5%, 8%, .773);
            font-size: var(--fs-500);
            text-transform: capitalize;
            font-family: var(--ff-heading);
        }
    }

    p {
        color: #767676;
        font-size: var(--fs-400);
        font-weight: 500;
        font-family: var(--ff-body);
    }
}

.stack {
    display: flex;
    gap: 1rem;
    justify-content: center;

    .stack-item {
        display: block;
        padding: 0.5rem;
        font-family: var(--ff-body);
        font-size: var(--fs-500);
        font-weight: 600;
    }
}

.links {
    margin-top: 1rem;

    .link-btn {
        font-size: var(--fs-400);
    }
}

@include lg {

    .projects-content {

        >h3 {
            text-align: left;
        }

        >p {
            text-align: left;
        }
    }

    .project-showcase {
        &:nth-child(even) {
            grid-template-columns: 45% 55%;

            .project-description {
                grid-column-start: 1;
                grid-row-start: 1;
            }
        }

        grid-template-columns: 55% 45%;
        align-items: center;
    }

    .project-description {
        margin: 2rem 0;
    }
}</style>