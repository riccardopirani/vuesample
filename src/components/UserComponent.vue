<template>
<div>
    <h1>{{ msg }}</h1>
</div>
</template>

<script>
import axios from "axios";
export default {
    name: "UserComponent",
    props: {
        msg: String,
    },
};
</script>
