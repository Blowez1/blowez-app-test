<template>
    <ul>
        <h2>Schools</h2>
        <li v-for="school in schools" :key="school.name">
            <a :href="school.web_pages[0]" target="_BLANK">{{school.name}}</a>
        </li>
    </ul>
</template>
<script>
export default {
    props : {
        schools : Array
    }
}
</script>