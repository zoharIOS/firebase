**install Firebase tools**

```
> npm i -g firebase-tools
'''

check if it install if it response to the command ```> firebase ```

login
```
> firebase login
```
**Local Firebase project**: create a project, cd to that directory and then:
```
>firebase init
```
selecgt the tool you like:
 ◯ Database: Deploy Firebase Realtime Database Rules
 ◯ Firestore: Deploy rules and create indexes for Firestore
❯◯ Functions: Configure and deploy Cloud Functions
 ◯ Hosting: Configure and deploy Firebase Hosting sites
 ◯ Storage: Deploy Cloud Storage security rules
```

After editing the project, go to [console.firebase]<https://console.firebase.google.com>  select functions 
because this is what we initiated, and copy the project ID from the url.
example" https://console.firebase.google.com/u/0/project/one-time-password-b07e6/functions/list
the project id is one-time-password-b07e6

deploy: local to remote project:
```
> firebase deploy --project one-time-password-b07e6
```

Now we can edit functions in remote project, in functions section.
the output will be displayed url:
```
Function URL (helloWorld): https://us-central1-one-time-password-b07e6.cloudfunctions.net/helloWorld
```

Inside the local project, in functions folder, index.js
every time we call expende with a name following, it will become as the name of a function.
```
exports.helloWorld = functions.https.onRequest((request, response) => {
 response.send("Hello from Firebase!");
});
```
hellloWorld is the name of the function that will apear in firbase console. the output "Hello from Firebase"
will be show in the url: https://us-central1-one-time-password-b07e6.cloudfunctions.net/helloWorld

if you get error, link the project in local to the relevant project in remote before deplying:
```
> firebase use --add
(select project from the list)
```
and then just ```firebase deploy```

