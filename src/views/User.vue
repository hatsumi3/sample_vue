<template>
  <div>
    <p>user</p>
    <router-link to="profile">profile</router-link> |
    <router-link to="post">post</router-link>
    <div class="green-b">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  name: "User",
};
</script>

<style>
.green-b {
  border: 1px green solid;
}
</style>
