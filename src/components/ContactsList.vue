<template>
  <div>
    <form @submit.prevent="addContact">
      <label>First name</label>
      <input v-model="newContact.first_name" type='text' placeholder="Firstname"/>
      <label>Last name</label>
      <input v-model="newContact.last_name" type='text' placeholder="Lastname"/>
      <label>Email</label>
      <input v-model="newContact.email" type="email" placeholder="Email"/>
      <button type='submit'>Submit</button>
      </form>
    <table>
      <thead>
        <th>First name</th>
        <th>Last name</th>
        <th>Email</th>
      </thead>
      <tbody>
        <tr v-for= "(contact, key) in contacts" :key="key">
          <td>{{ contact.first_name }}</td>
          <td>{{ contact.last_name}}</td>
          <td>{{ contact.email}}</td>
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
      contacts: [
        { first_name: 'Marko', last_name: 'Popovic',  email: 'nesto@exm.com'},
        { first_name: 'Marko1', last_name: 'Popovic1', email: 'nesto1@exm.com'},
        { first_name: 'Marko2',  last_name: 'Popovic2', email: 'nesto2@exm.com'}
      ],
      newContact: {
        first_name:'',
        last_name:'',
        email:''
      }
    }
  },
  methods:{
    addContact(){
      this.contacts.push(this.newContact)
      this.newContact = {}
      }
    }
  }

</script>


