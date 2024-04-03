<template>
  <div>
    <table class="users-table">
      <thead>
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>UserName</th>
          <th>Email</th>
          <th>Address</th>
          <th>Phone</th>
          <th>Website</th>
          <th>Company</th>
        </tr>
      </thead>
      <tbody>
        <td>1</td>
        <td>Joe</td>
        <td>user_joe</td>
        <td>user_joe@gmail.com</td>
        <td>CA USA</td>
        <td>+9595959595</td>
        <td><a href="#" target="_blank">www.website.com</a></td>
        <td>Testbla</td>
      </tbody>
    </table>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.users-table {
  border-collapse: collapse;
}

.users-table th,
.users-table td {
  border: 1px solid #fff;
  padding: 8px;
}
</style>
