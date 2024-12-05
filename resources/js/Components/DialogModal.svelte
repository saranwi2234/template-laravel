<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    import Modal from './Modal.svelte';

    export let show = false;
    export let maxWidth: 'sm' | 'md' | 'lg' | 'xl' | '2xl' = '2xl';
    export let closeable = true;

    const dispatch = createEventDispatcher();
</script>

<Modal {show} {maxWidth} {closeable} on:closed={() => dispatch('closed')}>
    <div class="px-6 py-4">
        <div class="text-lg font-medium text-gray-900">
            <slot name="title" />
        </div>

        <div class="mt-4 text-sm text-gray-600">
            <slot name="content" />
        </div>
    </div>

    <div class="flex flex-row justify-end bg-gray-100 px-6 py-4 text-end">
        <slot name="footer" />
    </div>
</Modal>
