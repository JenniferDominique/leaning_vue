<template>
    <section>
        <strong>
            {{  timePassad  }}
        </strong>
    </section>
</template>

<script lang="ts">
    import {defineComponent} from 'vue'

    export default defineComponent({
        name: 'Cronometro',
        props: {
            timeInSeconds: {
                type: Number,
                default: 0
            }
        },
        computed: {
            timePassad () : string {
                return new Date(this.timeInSeconds * 1000).toISOString().substr(11, 8)
            }
        },
    })
</script>