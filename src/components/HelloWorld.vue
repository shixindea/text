<script setup>
import { useTimeout, useVModel } from '@vueuse/core'
const props = defineProps(['name'])
const emit = defineEmits(['update:name'])

const data = useVModel(props, 'name', emit)
console.log('传递过来的值', data.value)
useTimeout(1000, {
  callback: () => {
    data.value = 'danke'
    console.log('执行1s', data.value)
  }
})
</script>
