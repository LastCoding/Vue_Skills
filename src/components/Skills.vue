<template>
    <div class="hello">
        <div class="holder">
            <ul>
                <li v-for="(data, index) in skills" :key="index">{{ index }}. {{ data.skill }}</li>
            </ul>

            <div v-bind:class="alertObject"></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Skills',
        data() {
            return {
                skills: [
                    {"skill": "Vue.js"},
                    {"skill": "Frotend Developer"}
                ],
                alertObject: {
                    alert: true,
                }
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .alert {
        background-color: yellow;
        width: 100%;
        height: 30px;
    }

    .another-class {
        border: 5px solid black;
    }

</style>
