<script lang="ts">
    export let id: string;
    export let checked = false;
</script>

<input
    {id}
    type="checkbox"
    bind:checked
    class="rounded border-gray-300 text-indigo-600 shadow-sm focus:ring-indigo-500"
    {...$$restProps}
/>
