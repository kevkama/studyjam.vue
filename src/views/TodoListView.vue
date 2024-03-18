<template>
    <div>
        <div id="todo">My Todo List</div>
        <hr />
        <div v-for="(task, index) in tasks" :key="index">
            <TaskView :title="task.title" :description="task.description" :status="task.status" :author="task.author" />
            <hr>
        </div>
    </div>
</template>


<script>
import TaskView from "../components/TaskView.vue"
export default {
    components: {
        TaskView,
    },
    data() {
        return {
            tasks: [
                {
                    title: "Wash Dishes",
                    description: "Wash dishes using liquid soap not powdered",
                    status: false,
                    author: "Mike",
                },
                {
                    title: "Clean Car",
                    description: "Clean car using liquid soap not powdered",
                    status: false,
                    author: "Rogers",
                },
                {
                    title: "Wash Shoes",
                    description: "Wash shoes using liquid soap not powdered",
                    status: true,
                    author: "Willy",
                },
                {
                    title: "Clean Shop",
                    description: "Clean shop using liquid soap not powdered",
                    status: false,
                    author: "Alex",
                },
            ],
        };
    },
};
</script>


<style scoped>
#todo {
  font-size: 36px;
  color: yellow;
  font-weight: bold;
}

</style>