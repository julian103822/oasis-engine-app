<script setup lang="ts">
    defineProps<{
        modelValue: String
    }>()
    defineEmits(['update:modelValue'])
    const attrs = useAttrs()
    console.log('attrs==', attrs)
</script>
<script lang="ts">
    export default{
        inheritAttrs: false
    }
</script>

<template>
    <div>
        <BaseTitle />
        <p>{{$attrs}}</p>
        <input
            class="my-input"
            v-bind="$attrs"
            :value="modelValue"
            @input="$emit('update:modelValue', $event.target.value)"
        />
    </div>
    
</template>
<style scope>
    .my-input{
        margin-top: 20px;
        border: 1px solid #999;
    }
</style>