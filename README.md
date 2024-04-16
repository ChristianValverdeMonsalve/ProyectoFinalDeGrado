# ProyectoFinalDeGrado

### User Signup / Login

| METHOD |      ENDPOINT     | TOKEN | ROLE |     DESCRIPTION      |            POST PARAMS          |         RETURNS        | 
|--------|-------------------|-------|------|----------------------|---------------------------------|-------------------------|
| POST   | /auth/signup      | -     | user | User Signup          | `DNI`, `username`, `usersurname`, `email`,`password`, `rol`, | { token: `token` }  |
| POST   | /auth/login       | -     | user | User Login           | `email`,`password`              | { token: `token` }      |

