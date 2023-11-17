<template>
    <Layout>
        <template #header>
            <Header></Header>
        </template>
        <template #resume>
            <Resume
            :label="'Ahorro total'"
            :date-label="dateLabel"
            :total-amount="100000"
            :amount="amount"
            >
                <template #graphic>Graphic</template>
                <template #action>Action</template>
            </Resume>
        </template>
        <template #movements>
            <Movements/>
        </template>
    </Layout>
</template>

<script>
import Layout from './Layout.vue';
import Header from './Header.vue';
import Resume from '@/components/resume/Index.vue'
import Movements from "./Movements.vue";

export default {
    components: {
        Layout,
        Header,
        Resume,
        Movements,
    },
    data() {
        return {
            amount: null,
            dateLabel: null,
        }
    }
}
</script>