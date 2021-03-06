# 7. Deploy AngularFire to Firebase

### 0. Build your Angular project for production

Before you can deploy your angular project, you need to build a version with your prod environment variables.
Make sure to add your production firebase configuration to the src/environments/environment.prod.ts before you build.

```bash
# build the angular project, creates a dist folder in your directory
ng build --prod
```

### 1. Initializing a Firebase project

You must initialize Firebase Hosting in order to deploy your application. In order to do this, run the `firebase init` command.

Note: If you haven't installed the Firebase CLI yet, run this command:

```bash
npm install --global firebase-tools
```

- This command prompts you to enter a public directory. Enter `dist` (generated by `ng build -prod`).
- The command will also ask you if you want to overwrite your index file. Type `n` since your Angular app includes an index file.
- This command also prompts you whether to configure the project as a single-page app. Enter `y` if you're using Angular Router or similar. Otherwise, enter `n`.

### 2. Deploy your Project

To deploy your app, simply run `firebase deploy`!

For more information on Firebase `init` and `deploy` commands, check out the [Firebase CLI documentation](https://firebase.google.com/docs/cli/).
