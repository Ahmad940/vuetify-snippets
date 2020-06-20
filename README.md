# vuetify-snippets
Vuetifyjs UI components is an awesome project isn't it? But, do you find it difficult or hard to remember the basic syntax for all the components it provides. So, this simple extension is here to help you solving this problem with lot of code intellisense.
## Installation


#### Browse for extension
You can browse and install vuetify-snippets from within vscode. Bring up the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of vscode or the View: Extensions command
 __(Ctrl+Shift+X)__ for Window users and __⇧⌘X__ for Mac users.
```
## Usage
To use this extension is very simply, just follow the sample code below
 
vbtn + [tab] =>  <v-btn small elevation="" color=""></v-btn>
vapp + [tab] => 
<v-app>
  <v-navigation-drawer app>
  </v-navigation-drawer>
  <v-app-bar app>
  </v-app-bar>
  <v-main>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
  </v-main>
  <v-footer app>
  </v-footer>
</v-app>

vlogin + [tab] => <template>
      <v-container fluid>
        <v-row class="text-center">
          <v-col cols="3" sm="2" md="3"></v-col>
          <v-col cols="12" sm="8" md="6">
            <v-card elevation="11" class="pt-10">
              <h2 class="purple--text text-uppercase">{{ title }}</h2>
              <v-divider color="purple" class="mt-2"></v-divider>
              <v-form
                @submit.prevent="onLogin"
                ref="form"
                v-model="valid"
                lazy-validation
                class="mt-10 mb-6 pr-8 pl-8 pb-8 pt-4"
              >
                <v-text-field
                  v-model="email"
                  append-icon="mail_outline"
                  outlined
                  color="purple"
                  error-count="2"
                  :rules="emailRules"
                  label="E-mail"
                  required
                ></v-text-field>
                <v-text-field
                  v-model="password"
                  color="purple"
                  :rules="passwordRules"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  @click:append="show1 = !show1"
                  :type="show1 ? 'text' : 'password'"
                  label="Password"
                  outlined
                  required
                ></v-text-field>

                <v-btn
                  x-large
                  type="submit"
                  block
                  :disabled="!valid"
                  color="purple darken-4"
                  class="mr-4 text"
                  @click="validate"
                >
                  <span class="white--text">Login</span>
                  <v-icon light>cached</v-icon>
                </v-btn>
              </v-form>
            </v-card>
          </v-col>
          <v-col cols="3" sm="2" md="3"></v-col>
        </v-row>
      </v-container>
    </template>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    title: "Login",
    valid: true,
    show1: false,
    show2: false,
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail must be valid"
    ],
    password: "",
    passwordRules: [
      v => !!v || "Password is required",
      v => (v && v.length >= 8) || "Password must be less than 8 characters"
    ]
  }),

  methods: {
    //..validate inputs
    validate() {
      this.refs.form.validate();
    },
    //Login method here
    onLogin() {
      //api call here
    }
  }
};
</script>

<style scoped>
</style

vcontainer + [tab] =>  <v-container class="">
    <v-row>
      <v-col></v-col>
    </v-row>
  </v-container>

and more of it
```

## Features
This extension provides snippets with the basic and advanced usage syntax for the most used components of vuetifyjs UI Components.
All you need to do is start typing the component's name all in lowercase and press tab. (all components logic will follow).


## Requirements
To be able to enjoy this extension your vscode engine must be         "vscode": "^1.46.0"


## Roadmap
This extension is intended to cover all the basic and advanced components with UI scaffold with quality code intellisense with the following.
- Vue-html support
- Html support
- Vue-jade support
- and more


## Contribution Guide
This extension is still under development. Please don't get angry if you don't find a given component and feel free to contribute instead. all sorts of contributions are welcome. Here are some guidelines to follow when submitting a contribution(s).
+ If you find a bug or you have a suggestion, feel free to open an issue for it.
+ If you want to add a new snippet or fix an existing bug, please open an issue for that (if it is not already open) and indicate that you are working on it to avoid working on the same issue by other developers.
+ Make sure to keep snippets organized according to the official documentation of vuetifyjs.
+ Snippet prefix must be the lowercase version of the component's name  without the dash(-) exp: v-btn => vbtn.
+ Snippet body must include only the most used properties available in the vuetifyjs documentation. Component docs is enough in most cases.
+ Snippet description can be the doc description of the component if it is small or just a meaningful part of it if it is long.


## License
This extension is license under MIT

> Again, your contributions of all sorts are most welcome.
**Enjoy**, Cheers🙂!









