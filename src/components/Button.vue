<template>
    <button @click="onClick()" :style="{background: color }" class ="btn">{{ text }}</button>
</template>
<script>
export default{
    name:'Button',
    props: {
        text: String,
        color: String,
    },
    methods: {
        //ich konnte nicht den DarkMode einbauen 
        onClick() {
            
            console.log('dark mode')
        },
    },
}
</script>