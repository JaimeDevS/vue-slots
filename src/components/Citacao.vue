<template>
    <div class="citacao">
        <slot name="fonte" ></slot>
        <slot></slot>
        <div class="autor">
            <slot name="autor"></slot>
        </div>
    </div>
</template>

<script>
export default {
    created() {
        console.log('created')
    },
    destroyed() {
        console.log('cerated')
    },
    /**
     * os métodos activated e deactivated
     * só vão funcionar quando o keep-alive estiver definido
     */
    activated() {
        console.log('activated')
    },
    deactivated() {
        console.log('deactivated')
    },
}
</script>

<style scoped>
    .citacao {
        border: 1px solid #DDD;
        background-color: rgba(0, 0, 0, .1);
        padding: 25px;
        max-width: 450px;
    }

    .autor {
        float: right;
    }
</style>
