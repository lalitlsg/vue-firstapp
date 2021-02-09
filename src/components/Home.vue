<template>
    <div>
        <h1 v-if="show">Hello from Home {{name}}</h1>
        <h1 v-else>Else Part</h1>
        <button v-on:click="handleShow">Click</button>
        <table>
            <tr>
                <th>Firstname</th>
                <th>Lastname</th>
            </tr>
            <tr v-for="user in users" :key="user.id">
                <td>{{user.firstname}}</td>
                <td>{{user.lastname}}</td>
            </tr>
        </table>
    </div>
</template>

<script>
    export default {
        name: 'Home',
        props: {
            name: String
        },
        data(){
            return {
                show: true,
                users: [
                    {id:1, firstname:"Lalit", lastname:"Garghate"},
                    {id:2, firstname:"Nikhil", lastname:"Patne"},
                    {id:3, firstname:"Pranay", lastname:"Tiwari"},
                ]
            }
        },
        methods: {
            handleShow(){
                this.show = !this.show
            }
        }
        
    }
</script>

<style lang="scss" scoped>

</style>