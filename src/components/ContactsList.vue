<template>
  <div>
    <table>
      <thead>
        <th>First name</th>
        <th>Last name</th>
        <th>Email</th>
      </thead>
      <tbody>
        <tr v-for= "(user, key) in users" :key="key">
          <td>{{ user.first_name }}</td>
          <td>{{ user.last_name}}</td>
          <td>{{ user.email}}</td>
        </tr>
      </tbody>
    </table>

  </div>
</template>

<script>
export default {
  name: 'ContactsList',
  data() {
    return {
      users: [
        { first_name: 'Marko', last_name: 'Popovic',  email: 'nesto@exm.com'},
        { first_name: 'Marko1', last_name: 'Popovic1', email: 'nesto1@exm.com'},
        { first_name: 'Marko2',  last_name: 'Popovic2', email: 'nesto2@exm.com'}
      ]
    }
  }
}
</script>


