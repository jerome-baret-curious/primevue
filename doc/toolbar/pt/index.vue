<template>
    <div class="doc-main">
        <div class="doc-intro">
            <h1>Toolbar Pass Through</h1>
        </div>
        <DocSections :docs="docs" />
    </div>
    <DocSectionNav :docs="docs" />
</template>

<script>
import DocApiTable from '@/components/doc/DocApiTable.vue';
import { getPTOption } from '@/components/doc/helpers/PTHelper.js';
import PtDoc from './PTDoc.vue';
import PTImage from './PTImage.vue';

export default {
    data() {
        return {
            docs: [
                {
                    id: 'pt.image',
                    label: 'Image',
                    description: 'Pass Through Image',
                    component: PTImage
                },
                {
                    id: 'pt.doc',
                    label: 'Toolbar Elements',
                    component: DocApiTable,
                    data: getPTOption('Toolbar')
                },
                {
                    id: 'pt.demo',
                    label: 'Demo',
                    description: 'Pass Through Demo',
                    component: PtDoc
                }
            ]
        };
    }
};
</script>
