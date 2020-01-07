<template>
  <v-container id="dropdown">
    <v-row :align="center" :justify="justify">
      <v-col justify="center" cols="4" sm="4">
        <div class="text-center">
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-select :items="['FunFunFunComp', 'BarBarBarComp', 'FizzFizzFizzComp', 'BuzzBuzzBuzzComp']" label="Company">
                <template v-slot:item="{ item, attrs, on }">
                  <v-list-item v-bind="attrs" v-on="on">
                    <v-list-item-title :id="attrs['aria-labelledby']" v-text="item"></v-list-item-title>
                  </v-list-item>
                </template>
              </v-select>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
        <br />
        <div class="text-center">
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-select :items="['FooFooFooApp', 'BarBarBarAPp', 'FizzFizzFizzFizzApp', 'BuzzBuzzBuzzApp']" label="Application">
                <template v-slot:item="{ item, attrs, on }">
                  <v-list-item v-bind="attrs" v-on="on">
                    <v-list-item-title :id="attrs['aria-labelledby']" v-text="item"></v-list-item-title>
                  </v-list-item>
                </template>
              </v-select>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
        <br/>
          <div class="text-center">
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-select :items="['Dev', 'Test', 'Prod']" label="Environment">
                <template v-slot:item="{ item, attrs, on }">
                  <v-list-item v-bind="attrs" v-on="on">
                    <v-list-item-title :id="attrs['aria-labelledby']" v-text="item"></v-list-item-title>
                  </v-list-item>
                </template>
              </v-select>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
      </v-col>
    </v-row>
    <v-divider class="my-3"></v-divider>
            
  </v-container>
</template>

<script>
export default {
  data: () => ({
    alignment: "center",
    justify: "center"
  })
};
</script>

<style>
.my-3 {
  margin-left: 1%;
  margin-right: 1%;
}

.btn {
  width: 100%;
  min-width: 100%;
}

h4 {
  color: gray;
}
</style>