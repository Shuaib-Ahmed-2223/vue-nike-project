<script setup>
import { defineProps, defineEmits } from 'vue';

// Props
const props = defineProps({
  imgURL: {
    type: Object,
    required: true,
  },
  bigShoeImg: {
    type: String,
    required: true,
  },
});

// Event emit setup
const emit = defineEmits(['changeBigShoeImage']);

// Handle click function
const handleClick = () => {
  if (props.bigShoeImg !== props.imgURL.bigShoe) {
    emit('changeBigShoeImage', props.imgURL.bigShoe);
  }
};
</script>

<template>
  <div
    :class="[
      'border-2 rounded-xl cursor-pointer max-sm:flex-1',
      bigShoeImg === imgURL.bigShoe ? 'border-coral-red' : 'border-transparent'
    ]"
    @click="handleClick"
  >
    <div class="flex justify-center items-center bg-card bg-center bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4">
      <img
        :src="imgURL.thumbnail"
        alt="shoe collection"
        width="127"
        height="103.34"
        class="object-contain"
      />
    </div>
  </div>
</template>
  

  
  <style scoped>
  /* Add your styles here if necessary */
  </style>
  