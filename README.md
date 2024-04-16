# ProyectoFinalDeGrado

### User Signup / Login

| METHOD |      ENDPOINT     | TOKEN | ROLE |     DESCRIPTION      |            POST PARAMS          |         RETURNS         | 
|--------|-------------------|-------|------|----------------------|---------------------------------|-------------------------|
| POST   | /auth/signup      | -     | user | User Signup          | `DNI`, `username`, `userlastname`, `email`,`password`, `role`, | { token: `token` }  |
| POST   | /auth/login       | -     | user | User Login           | `email`,`password`              | { token: `token` }      |


### User Endpoints

| METHOD |      ENDPOINT     | TOKEN | ROLE |     DESCRIPTION      |            POST PARAMS          |         RETURNS         |
|--------|-------------------|-------|------|----------------------|---------------------------------|-------------------------|
| GET    | /user             | YES   | admin| Get All Users        | `query params`                  | [{user}]                |
| GET    | /user/profile     | YES   | user | Get Own Profile      |                                 | {user}                  |
| GET    | /user/:userId     | YES   | admin| Get One User         |                                 | {user}                  |
| POST   | /user             | YES   | admin| Create one User      | `DNI`, `username`, `userlastname`, `email`, `password`, `role`| {user} |
| PUT    | /user/profile     | YES   | user | Update own profile   | `DNI`, `username`, `userlastname`,`email`, `password`, `role`, `committee`| {message: 'Profile updated'}|
| PUT    | /user/password    | YES   | user | Reset password       | `newPassword`, `repeatPassword` | { message: 'Password updated' } |
| PUT    | /user/:userId     | YES   | admin| Update one user      | `DNI`, `username`, `userlastname`,`email`, `password`, `role`| {message: 'User updated'} |
| DELETE | /user/:userId     | YES   | admin| Delete one user      |                                 | {message: 'User deleted'} |
