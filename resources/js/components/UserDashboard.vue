<template>
    <div class="user-dashboard">
        <div class="list-user-comp">
            <h4>List User</h4>
            <!-- Listen event 'userSelected' emitted from child and process it using 'childrenSelectUser' -->
            <UserList @userSelected="childrenSelectUser('this is test string', ...arguments)"></UserList>
        </div>
        <hr>
        <div class="user-detail-comp">
            <h4>User Detail</h4>
            <!-- pass 'userSelectedFromChild', child will use props 'userDetailInfo' -->
            <UserDetail :userDetailInfo="userSelectedFromChild"></UserDetail>
        </div>
    </div>
</template>

<script>
    import UserList from './UserList.vue'
    import UserDetail from './UserDetail.vue'
    export default {
        components: {
            UserList,
            UserDetail
        },
        data() {
            return {
                userSelectedFromChild: {}
            }
        },
        methods: {
            // Process event emitted from child
           childrenSelectUser(text, user, number, string) {
                console.log(text)
                console.log(user)
                console.log(number)
                console.log(string)
                this.userSelectedFromChild = user
            }
        }
    }
</script>

<style lang="scss" scoped>
</style>