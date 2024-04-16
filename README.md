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

### Class Endpoint

| METHOD |      ENDPOINT     | TOKEN | ROLE |     DESCRIPTION      |            POST PARAMS          |         RETURNS         |
|--------|-------------------|-------|------|----------------------|---------------------------------|-------------------------|
| GET    | /class            | YES   | admin| Get All Classes      | `query params`                  | [{clases}]              |
| GET    | /class            | YES   | user | Get All Classes      | `query params`                  | [{clases}]              |
| GET    | /class/:classId   | YES   | admin| Get One Class        |                                 | {class}                 |
| GET    | /class/:classId   | YES   | user | Get One Class        |                                 | {class}                 |
| POST   | /class            | YES   | admin| Create one Class     | `classId`, `className`, `timeTable`, `duration`, `monitorId`, `maxUsers`, `currentUsers`| {class} |
| PUT    | /class/:classId   | YES   | admin| Update one Class     |`classId`, `className`, `timeTable`, `duration`, `monitorId`, `maxUsers`, `currentUsers` | {message: 'Class updated'} |
| DELETE | /class/:classId   | YES   | admin| Delete one Class     |                                 | {message: 'Class deleted'} |

### Booking Endpoint

| METHOD |       ENDPOINT      | TOKEN | ROLE |     DESCRIPTION      |            POST PARAMS          |         RETURNS         |
|--------|---------------------|-------|------|----------------------|---------------------------------|-------------------------|
| GET    | /booking            | YES   | admin| Get All Bookings     | `query params`                  | [{bookings}]            |
| GET    | /booking/:bookingId | YES   | admin| Get One Booking      | `query params`                  | {booking}               |
| GET    | /booking/profile    | YES   | user | Get Own Bookings     | `query params`                  | {bookings}              |
| POST   | /booking            | YES   | admin| Create One Booking   | `userId`, `classId`, `date_time`| {booking}               |
| POST   | /booking/profile    | YES   | user | Create Own Booking   | `userId`, `classId`, `date_time`| {booking}               |
| PUT    | /booking/:bookingId | YES   | admin| Update One Booking   | `userId`, `classId`, `date_time`| {message: 'Booking updated'} |
| PUT    | /booking/:bookingId | YES   | user | Update Own Booking   | `userId`, `classId`, `date_time`| {message: 'Booking updated'} |
| DELETE | /booking/:bookingId | YES   | admin| Delete One Booking   |                                 | {message: 'Booking deleted'} |
| DELETE | /booking/:bookingId | YES   | user | Delete Own Booking   |                                 | {message: 'Booking deleted'} |








