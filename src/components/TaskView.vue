<template>
    <div id="task">
        <div id="title">{{ title }}</div>
        <div id="description">{{ description }}</div>
        <div id="status">

            <div v-show="status">complete: 👯</div>
            <div v-show="!status">complete: 😥</div>
        </div>
        <div id="author">{{ author }}</div>
    </div>
</template>



<script>
export default{
    props:["title","description","status","author"],
};
</script>


<style scoped>
#task{
    margin:10px;
}
#title{
    font-size: 24px;
    font-weight: bold;
    text-align: start;
}

#description{
    font-size: 20px;
    text-align: start;
}

#status{
    font-size: 18px;
    text-align: start;
}

#author{
    font-size: 16px;
    text-align: start;
    padding: 4px;
}
</style>