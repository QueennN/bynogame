<template>
    <div class="flex  flex-wrap items-center justify-center">
        <by-card
            v-for="(item, i) in data"
            :key="i"
            :_id="item.id"
            :_image="item.url"
            :_download="item.download_url"
            :_author="item.author"
        />
    </div>
</template>

<script>
import card from "../components/card/card";
import axios from "axios";
export default {
    components: { "by-card": card },
    data() {
        return {
            data: []
        };
    },
    mounted() {
        axios.get("https://picsum.photos/v2/list?page=1&limit=10").then(res => {
            this.data = res.data;
        });
    }
};
</script>
