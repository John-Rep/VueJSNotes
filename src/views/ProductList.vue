<script lang="ts">
import { computed, ref } from 'vue'

export default{
    name: 'ProductList',
    props: {
        id: {
            type: Number,
            default: 1,
        },
        label: {
            type: String,
            default: "No Label",
        },
        description: {
            type: String,
            default: "No Description",
        },
        quantity: {
            type: Number,
            default: 5,
        },
    },
    setup(props) {
        const id = props.id
        const label = props.label
        const desc = props.description
        const status = computed(() => {
            return props.quantity > 0 ? "Available" : "Unavailable"
        })

        return {
            id,
            label,
            desc,
            status,
        }
    },
}
</script>
<template>
    <tr>
        <td>{{ id }}</td>
        <td>{{ label }}</td>
        <td>{{ desc }}</td>
        <td>{{ status }}</td>
    </tr>
</template>
<style></style>