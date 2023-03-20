  
<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import { defineComponent } from 'vue';
import '@splidejs/vue-splide/css';

export default defineComponent({
    data() {
        return {
            profiles: {
                profile_1: {
                    name: "Name1",
                    bio: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.`,
                    hobby: "Hobby1",
                    age: "TBD",
                    image: "../../images/profile.png"
                },
                profile_2: {
                    name: "Name2",
                    bio: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.`,
                    hobby: "Hobby2",
                    age: "TBD",
                    image: "../../images/profile.png"
                },
                profile_3: {
                    name: "Name3",
                    bio: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.`,
                    hobby: "Hobby3",
                    age: "TBD",
                    image: "../../images/profile.png"
                }

            },
            observations: {
                observation_1: {
                    author: "Name1",
                    observation: `Observation 1`
                },
                observation_2: {
                    author: "Name1",
                    observation: `Observation 2`
                },
                observation_3: {
                    author: "Name2",
                    observation: `Observation 3`
                },
                observation_4: {
                    author: "Name2",
                    observation: `Observation 4`
                },
                observation_5: {
                    author: "Name3",
                    observation: `Observation 5`
                },
                observation_6: {
                    author: "Name3",
                    observation: `Observation 6`
                }
            },
            logo: {
                element_1: {
                    img: "../../images/foundation.svg",
                    description: `Foundation is a free and open-source responsive front-end
                    framework, providing a responsive grid and HTML and CSS UI. This framework 
                    was used in this project for the general responsive formatting of the page
                    as well as providing a nice looking UI. `,
                    assetName: "Foundation"
                },
                element_2: {
                    img: "../../images/jQuery.png",
                    description: `jQuery is a free and open-source library
                    designed to simplify HTML DOM tree traversal and 
                    manipulation. This resource was used in getting 
                    conditions from UI controls and updating the crime table
                    based on the map conditions. `,
                    assetName: "jQuery"
                },
                element_3: {
                    img: "../../images/leaflet.png",
                    description: `Leaflet is a open-source library used to build
                    web mapping applications. This framework was used immensely in the
                    creation of the map, the placing of search and neighborhood tags 
                    on the map and updating based UI controls.`,
                    assetName: "Leaflet"
                },
                element_4: {
                    img: "../../images/nominatim.png",
                    description: `Nominatim, otherwise referred to as OpenStreetMap (OSM) 
                    is a collaborative project to create a free editable database of the world. 
                    This database was queried through the nominatim API to retrieve data about 
                    the St. Paul, Minnesota area. The marker popups displays this data.`,
                    assetName: "Nominatim"
                },
                element_5: {
                    img: "../../images/splide.png",
                    description: `Splide is a lightweight, flexible and accessible
                    slider/carousel written in Typescript. There are no dependencies so 
                    one can simply plug and play. It was used to create the gallery element 
                    that this description is in.`,
                    assetName: "Splide"
                },
                element_6: {
                    img: "../../images/turf.jpg",
                    description: `Turf is a framework that is used for advanced geospatial
                    analysis. It was created especially for browsers and Node.js. This 
                    framework had a very simple function which was to merge all the neighborhood
                    polygons together to create a larger polygon to clamb the bounds to remain inside
                    the St. Paul area.`,
                    assetName: "turf"
                },
                element_7: {
                    img: "../../images/vue.png",
                    description: `Derived from AngularJS, Vue is a performant and versatile
                    framework for building web user interfaces. It builds on top of standard 
                    HTML, CSS, and JavaScript to make development easier and less cumbersome. 
                    It was used in the main organization of this project.`,
                    assetName: "Vue"
                }
            }
        }
    },
    components: { Splide, SplideSlide },
});

</script>

<template>
    <div style="background-color: rgba(255,255,255,0.5); ">
        <div class="grid-x">

            <div class="large-12 medium-12 small-12 cell">
                <!-- User profiles will go here -- try to use some hoverable note cards -->

                <div id="large-12 medium-12 small-12 cell">
                    <div id=content-header>
                        <h4>Meet the Team</h4>
                    </div>
                </div>
                <div class="flex">
                    <div v-for="element in profiles">
                        <div class="card">
                            <img class="bio_image" :src="element.image" :alt="element.name + 'Profile Picture'">
                            <h2>{{ element.name }}</h2>
                            <h3>Age: {{ element.age }}</h3>
                            <h3>Hobby: {{ element.hobby }}</h3>
                            <p>Bio: {{ element.bio }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-x">
            <div class="large-12 medium-12 small-12 cell">
                <div id="large-12 medium-12 small-12 cell">
                    <div id=content-header>
                        <!-- <h4>Video</h4> -->
                    </div>
                </div>
                <div class="flex">
                    <!-- <iframe width="560" height="315" src="" -->
                    <!-- title="YouTube video player" frameborder="0" -->
                    <!-- allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" -->
                    <!-- allowfullscreen></iframe> -->
                </div>
            </div>
        </div>
        <div class="grid-x">
            <div class="large-12 medium-12 small-12 cell">
                <div id="large-12 medium-12 small-12 cell">
                    <div id=content-header>
                        <h4>Observations</h4>
                    </div>

                </div>
                <div id="table_div">
                    <table>
                        <tr>
                            <th>Author</th>
                            <th>Observation</th>
                        </tr>
                        <tr v-for="element in observations">
                            <td class="table-data">{{ element.author }}</td>
                            <td class="table-data">{{ element.observation }}</td>
                        </tr>
                    </table>
                </div>

            </div>
        </div>
        <div class="grid-x">
            <div class="large-12 medium-12 small-12 cell">
                <div id="large-12 medium-12 small-12 cell">
                    <div id=content-header>
                        <h4>Frameworks/APIs</h4>
                    </div>
                </div>
            </div>
            <div class="large-1 medium-1 small-0 cell"></div>
            <div class="large-10 medium-10 small-12 cell">
                <div class="flex">
                    <div class="gallery-size">
                        <Splide :options="{ rewind: true, drag: 'free', width: 800 }" aria-label="Vue Splide Example">
                            <SplideSlide v-for="element in logo">
                                <div class="grid-x">
                                    <div class="image large-1 medium-1 small-1 cell"></div>
                                    <div class="image large-5 medium-5 small-5 cell">
                                        <img class="logo" :src=element.img alt="">
                                    </div>
                                    <div class="desc large-5 medium-5 small-5 cell">
                                        <div class="logo_header">
                                            <p>{{ element.assetName }}</p>
                                        </div>
                                        <p>{{ element.description }}</p>
                                    </div>
                                    <div class="image large-1 medium-1 small-1 cell"></div>
                                </div>
                            </SplideSlide>
                        </Splide>
                    </div>
                </div>
            </div>
        </div>
        <br><br><br>
    </div>
</template>

<style>
.gallery-size {
    /* max-width: 1000px; */
    display: flex;
    justify-content: center;
}

.logo {
    height: 300px;
    object-fit: cover;
    background-color: rgba(255, 255, 255, 0.5);
}

.logo_header {
    font-size: 1.3rem;
    text-decoration: underline;
    text-align: center;
}

.desc {
    height: 300px;
    max-width: 300px;
    padding: 1rem;
    background-color: rgba(200, 200, 200, 0.8);
}

.image {
    text-align: right;
    height: 100px;
}

.card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    max-width: 500px;
    margin: auto;
    text-align: center;
    border-radius: 20px;
    background-color: rgba(88, 107, 164, 0.8);
    border: 8px double black;
    transition: 1s;
}

.card:hover {
    background-color: rgba(255, 255, 255, 0.5);
    transform: scale(1.2)
}

.flex {
    display: flex;
    justify-content: space-evenly;
}

h2 {
    font-size: 1.5rem;
}

h3 {
    font-size: 1rem;

}

.bio_image {
    height: fit-content;
    max-height: 300px;
    border-radius: 50%;
    background-color: rgba(255, 255, 255, 0.7);
}

.table-data {
    background-color: rgba(250, 235, 215, 0.6);
}

#table_div {
    padding-left: 100px;
    padding-right: 100px;
}

h4 {
    font-size: 3rem;
    color: black;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    width: max-content;
    padding: 10px;
    background-color: rgba(119, 141, 206, 0.8);
    text-decoration: underline;
    border-radius: 20px;
}

#content-header {
    /* width: 100%; */
    text-align: center;
    display: flex;
    justify-content: center;
    padding: 20px;
}
</style>