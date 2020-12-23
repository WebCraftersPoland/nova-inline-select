<template>
    <modal>
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div>
                <heading
                    :level="3"
                    class="border-b border-40 p-6"
                >
                    {{ __('Confirm action') }}
                </heading>
                <p class="p-6">{{ __('Do you want to confirm this action?') }}</p>
            </div>
            <div class="bg-30 p-3 flex">
                <div class="flex items-center ml-auto">
                    <button
                        type="button"
                        class="btn btn-link text-80 cursor-pointer mr-6"
                        @click="$emit('close-modal')"
                    >
                        {{ __('Cancel') }}
                    </button>
                    <button
                        type="button"
                        class="btn py-2 px-4 btn-primary rounded"
                        @click="$emit('submit')"
                    >
                        {{ __('Confirm') }}
                    </button>
                </div>
            </div>
        </div>
    </modal>
</template>
<script>
    export default {
        name: 'confirm-modal'
    }
</script>
<style lang="scss" scoped>
    .modal {
        @media (max-width: 992px) {
            top: 100px;
        }
    }
</style>