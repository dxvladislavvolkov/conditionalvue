<script>
import { h } from 'vue';
export default {
    props: {
        opt2: String
    },
    render() {
        const slots = this.$slots && this.$slots.default && this.$slots.default() || [];
        return h("div", {}, slots)
    },
    mounted() {
        console.log(this.$slots.default()[0].children)
    }

}
</script>

<style>

</style>