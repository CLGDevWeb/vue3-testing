<template>
    <div>
        <button @click="toggleModal" type="button">Open modal</button>

        <div v-if="modalIsOpen" class="modal">
            <p>
                Modal is open !
            </p>
        </div>
    </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup () {
        const modalIsOpen = ref(false)

        return {
            toggleModal: () => modalIsOpen.value = !modalIsOpen.value
        }
    }
}
</script>