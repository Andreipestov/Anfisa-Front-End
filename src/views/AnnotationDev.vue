<template>
    <div class="annotation-dev">
        <SettingsPanel />
        <VariantsPanel />
        <VariantDetails />
    </div>
</template>

<script>
import SettingsPanel from '@/components/settingsPanel/SettingsPanel.vue';
import VariantsPanel from '@/components/variantsListPanel/VariantsPanel.vue';
import VariantDetails from '@/components/variantDetailsPanel/VariantDetailsPanel.vue';

export default {
    name: 'annotation-dev',
    components: {
        SettingsPanel,
        VariantsPanel,
        VariantDetails,
    },
    created() {
        this.$store.state.workspace = 'ANNOTATION SERVICE';
        this.$store.state.panels.variantsPanelCollapsed = true;
    },
    beforeDestroy() {
        this.$store.state.workspace = '';
    },
};
</script>

<style lang="scss">
    .annotation-dev {
        -webkit-font-smoothing: antialiased;
        display: flex;
        height: 100%;
        min-height: 600px;
        background-color: #f9f4e0;
    }
</style>
