<template>
  <h1>Log out</h1>
</template>
<script>
import axios from "axios";
export default {
  name: "Logout",
  created: function () {
    axios({
      method: "POST",
      url: "/api/auth/logout",
    }).then(() => {
      localStorage.removeItem("user");
      this.$router.push("/");
    });
  },
};
</script>
