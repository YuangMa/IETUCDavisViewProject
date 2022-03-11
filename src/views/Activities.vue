<template>
    <div v-if="activities.length">
        <div v-for="activity in activities" :key="activity.id" class="activity">
            <router-link :to="{name: 'ActivityDetails', params: {
                id: activity.id,
                title: activity.title,
                displayName: activity.actor.displayName,
                objectType: activity.object.objectType,
                published: activity.published}}">

                <h2>{{activity.title}} <br>
                    {{activity.actor.displayName}}</h2>
            
            </router-link>
        </div>
    </div>
    <div v-else>
        <p>Loading Activities...</p>
    </div>
</template>

<script>
export default{
    data(){
        return { 
            activities: []
        }
    },
    mounted(){
        fetch('https://aggiefeed.ucdavis.edu/api/v1/activity/public?s=0?l=25')
        .then(res => res.json())
        .then(data => this.activities = data)
        .catch(err => console.log(err.message))
    }
}
</script>

<style>
.activity h2{
    background: #f4f4f4;
    padding: 8px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 700px;
    cursor: pointer;
    color: #444;
    text-align: left;
}

.activity h2:hover {
    background: #ddd;
}

.activity a{
    text-decoration: none;
}

</style>