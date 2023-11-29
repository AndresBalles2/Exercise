<script setup>

const props = defineProps(
    {
    tarea: {
        type: String,
        default: 'Tarea por defecto'
    },
    index: {
        type: Number
    }
    }
)

const emit = defineEmits([ 'borrarHijo' ])

function borrar (index){
    //console.log('Borrar hijo', index)
    emit('borrarHijo', index)
}

</script>

<template>

    <div class="transition-colors duration-300 hover:bg-gray-300 mt-1 px-4 py-1 flex justify-between bg-gray-200 rounded">

    {{props.tarea}}

<span
@click="borrar(props.index)"
 class="px-2 transition-colors duration-300 hover:cursor-pointe hover:bg-red-900 hover:cursor-pointer  text-xl text-center text-white bg-red-600 rounded">
  X
</span>

</div>


</template>