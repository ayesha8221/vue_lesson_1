<template>
    <div v-if="tutorials" class="flex-container">
        <CardComp v-for="tutorial of tutorials" :key="tutorial.id" :tutorial="tutorial"/>
    </div>
    <div v-else>Loading...</div>
</template>
<script>
import CardComp from '@/components/CardComp.vue'
export default {


    components: { CardComp},

    computed: {

        tutorials() {
            return this.$store.state.tutorials
        }
    },
    mounted() {
        this.$store.dispatch("getTutorials")
    },
}
</script>