| Deadline         |
|------------------|
|                  |

# YouTube client app

[Figma mockup](https://www.figma.com/file/tS3Zqk138yXUmRxSWKDv4r/YouTube-client?node-id=0%3A1)

## Angular. NgRX
The objective of the task is to implement new page `admin`. So, your app will contain the following pages:
- Login page
- 404 page
- Main page (which is implemented before)
- Detailed information page
- Admin

**[YouTube client. Admin page JPG](https://github.com/rolling-scopes-school/tasks/blob/master/tasks/angular/admin.jpg)**

### Task requirements
In this task, you need to do the following:
- connect the NgRX library, create a storage (state), which will contain:
    - data about custom cards.
    - data about video from API YouTube.

- admin page with which you can add your own cards. Your own cards should contain the following information:
    - title
    - description
    - link to the image
    - link to video
    - creation date ( current date )

#### ⚠️ Warning!   
**When you enter new information into the input and receive a new response from the youtube api, the information about your own cards should be saved until your application is reloaded.**

#### Project structure and technical requirements
The project structure can be organized in the following way:

```
    app
    ├── core                
    │   ├── components
    │   ├── pages
    │   ├── services
    │   ├── guards
    ├── shared
    │   ├── components
    │   ├── directives
    │   ├── models
    │   ├── pipes
    ├── redux
    │   ├── actions
    │   ├── reducers
    │   ├── effects
    │   ├── reducers
    │   ├── selectors
    │   ├── state.models.ts
    ├── youtube
    │   ├── components
    │   ├── directives
    │   ├── models
    │   ├── pages
    │   ├── pipes
    │   ├── services
    ├── auth
    │   ├── components
    │   ├── models
    │   ├── pages
    │   ├── services
    ├── app.component.html
    ├── app.component.scss
    ├── app.component.ts
    ├── app.component.spec.ts
    ├── app.module.ts
```

#### Functional requirements
Now the logic of your application is as follows:
- You make a request to the youtube api.
- Get a response and make an array with data about YouTube videos from it.
- Display information in accordance with your template.

In this task, you need to connect the NgRX library and organize the storage of the received data. Your application should now work in the following scenario:
- You make a request to the youtube api.
- Get a response and make an array with data about YouTube videos from it.
- Save it to storage(state).
- In the application, you use the data that is in the storage (state) to draw cards only.

The storage can only be changed in the following cases:
- Received a new response from the youtube api.
- Added a new card on the admin page.

#### Evaluation criteria
Maximum points - **100**

- [ ] Implemented **Admin page** (**+10**)
- [ ] The **Admin page** functionality with necessary rules is implemented (**+10**)
- [ ] Created by storage (state) using the NgRX library (**+20**)
- [ ] Custom cards are saved in the store (**+30**)
- [ ] The data received from the API YouTube is stored in the store (**+30**)

Fines
- [ ] Failure to submit on time may lead to points lose according to the [Stage #2 requirements](https://docs.rs.school/#/stage2?id=%d0%94%d0%b5%d0%b4%d0%bb%d0%b0%d0%b9%d0%bd%d1%8b)
- [ ] The app has wrong project structure (**-20**)
- [ ] The app doesn't work or has console errors (**-20**)
- [ ] TSLint warnings or errors are present (**-15**)

### Useful links
https://ngrx.io  
https://ngrx.io/guide/store/configuration/runtime-checks  
https://ngrx.io/guide/store/actions  
https://ngrx.io/guide/store/reducers  
https://ngrx.io/guide/effects  