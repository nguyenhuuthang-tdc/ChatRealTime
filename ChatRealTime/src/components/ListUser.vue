<template>
    <div class="list-users">
        <h2 class="title">{{ content }}</h2>
        <user v-for="item in unActiveUser" v-bind:key="item.id" v-bind:users="item"/>
    </div>
</template>

<script>
import User from './Users.vue'
export default {
    name: "list-user",
    props: {
        listUser: {
            type: Array,
            default: []
        }
    },
    data() {
        return {
            content: "List User",
        }
    },
    computed: {
        activeUser() {
            return this.listUser.filter(function(user) {
                return user.active;
            })
        },
        unActiveUser() {
            var un_user = []
            this.listUser.forEach(user => {
                if(user.active === false) {
                    un_user.push(user)
                }
            });
            return un_user;
        }
    },
    components: {
        User
    }
}
</script>

<style>
    .title {
        position: relative;
    }
    .title::before {
        position: absolute;
        content: "";
        width: 120px;
        height: 2px;
        margin: 0px auto;
        left: 0;
        right: 0;
        top: 120%;
        background: #000;
    }
</style>
