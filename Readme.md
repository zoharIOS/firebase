**install Firebase tools**

```
> npm i -g firebase-tools
'''

check if it install if it response to the command ```> firebase ```

login
```
> firebase login
```
create a project, cd to that directory and then:
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

deploy:
```
> firebase deploy --project one-time-password-b07e6
```




