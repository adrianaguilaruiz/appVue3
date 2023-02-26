<script>
import SingleComponent from '../components/myComponents/SingleComponent.vue';
import RawHtmlComponent from '../components/myComponents/RawHtmlData.vue';
import DirectiveVShow from '../components/myComponents/directives/DirectiveVShow.vue';
import DirectiveVModel from '../components/myComponents/directives/DirectiveVModel.vue';
import DirectiveVFor from '../components/myComponents/directives/DirectiveVFor.vue';
import ParentComponent from '../components/myComponents/props/ParentComponent.vue';

export default { components: { SingleComponent, RawHtmlComponent, DirectiveVShow, DirectiveVModel, DirectiveVFor, ParentComponent } };
</script>
    
<template>
    <div>
        <h1>My Single Page from FemCoders</h1>
        <!-- <h3>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis aperiam itaque porro quaerat nisi, quo ducimus nobis ad eius debitis molestias voluptatem? Explicabo dolorem excepturi soluta quasi, alias dolore laboriosam.</h3> -->
        -------------------------
        <SingleComponent />
        -------------------------
        <RawHtmlComponent />
        -------------------------
        <DirectiveVShow />
        -------------------------
        <!-- <DirectiveVIf /> -->
        -------------------------
        <DirectiveVModel />
        -------------------------
        <DirectiveVFor />
        -------------------------
        <!-- <ComputedProps /> -->
        -------------------------
        <ParentComponent />
    </div>
</template>

<style lang="css" scoped>
    h1 {
        color: brown;
    }
</style>