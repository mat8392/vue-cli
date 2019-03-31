<template>
    <div class="jsonplaceholdertest">
        <show-blog></show-blog>
    </div>
</template>

<script>
import ShowBlogs from '@/components/ShowBlogs.vue';

export default {
    name: 'jsonplaceholdertest',
    components: {
        'show-blog': ShowBlogs
    },
    data() {
        return {};
    },
    methods: {}
};
</script>

<style scoped>
body {
    margin: 0;
    font-family: 'Nunito SemiBold';
}
</style>
