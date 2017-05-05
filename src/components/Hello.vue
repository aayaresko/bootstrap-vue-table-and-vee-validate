<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
    <b-table striped hover :items="items" :fields="fields" :current-page="currentPage" :per-page="perPage" :filter="filter">
      <template slot="name" scope="item">
        {{item.value.first}} {{item.value.last}}
      </template>
      <template slot="isActive" scope="item">
        {{item.value ? 'Yes :)' : 'No :('}}
      </template>
      <template slot="actions" scope="item">
        <b-btn size="sm" @click="details(item.item)">Details</b-btn>
      </template>
    </b-table>
  </div>
</template>

<script>
  export default {
    name: 'hello',
    data () {
      return {
        items: [{
          isActive: true,
          age: 40,
          name: {
            first: 'Dickerson',
            last: 'Macdonald'
          }

        }, {
          isActive: false,
          age: 21,
          name: {
            first: 'Larsen',
            last: 'Shaw'
          }

        }, {
          isActive: false,
          age: 9,
          state: 'success',
          name: {
            first: 'Mitzi',
            last: 'Navarro'
          }

        }, {
          isActive: false,
          age: 89,
          name: {
            first: 'Geneva',
            last: 'Wilson'
          }

        }, {
          isActive: true,
          age: 38,
          name: {
            first: 'Jami',
            last: 'Carney'
          }

        }, {
          isActive: false,
          age: 27,
          name: {
            first: 'Essie',
            last: 'Dunlap'
          }

        }, {
          isActive: true,
          age: 40,
          name: {
            first: 'Dickerson',
            last: 'Macdonald'
          }

        }, {
          isActive: false,
          age: 21,
          name: {
            first: 'Larsen',
            last: 'Shaw'
          }

        }, {
          isActive: false,
          age: 26,
          name: {
            first: 'Mitzi',
            last: 'Navarro'
          }

        }, {
          isActive: false,
          age: 22,
          name: {
            first: 'Geneva',
            last: 'Wilson'
          }

        }, {
          isActive: true,
          age: 38,
          name: {
            first: 'Jami',
            last: 'Carney'
          }

        }, {
          isActive: false,
          age: 27,
          name: {
            first: 'Essie',
            last: 'Dunlap'
          }

        }],
        fields: {
          name: {
            label: 'Person Full name',
            sortable: true
          },
          age: {
            label: 'Person age',
            sortable: true
          },
          isActive: {
            label: 'is Active'
          },
          actions: {
            label: 'Actions'
          }
        },
        currentPage: 1,
        perPage: 5,
        filter: null
      }
    },
    methods: {
      details (item) {
        alert(JSON.stringify(item))
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
