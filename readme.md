# PERSONNEL API

### ERD:

![ERD](./erdPersonnelAPI.png)

### Folder/File Structure:

```
    .env
    .gitignore
    index.js
    readme.md
    src/
        configs/
            dbConnection.js
        controllers/
            department.controller.js
            personnel.controller.js
        helpers/
            passwordEncrypt.js
        middlewares/
            errorHandler.js
            findSearchSortPage.js
        models/
            department.model.js
            personnel.model.js
        routes/
            department.router.js
            personnel.router.js
```

## Project Requirements

We will have Department and Personnel tables and we will link them to each other.
Each department will have its own personnel.
Each department will have only one Lead.
Admin or Lead; the response will change dynamically based on the request coming in the URL. In other words, when we want to list the personnel belonging to the departments, we will do this through a single URL: departments/id/personnels.
Admin will be able to perform CRUD operations for new personnel (by admin, we mean someone authorized, you can call this by a different name if you want).
Personnel can only read and update their own information but only the Admin will have the delete authority.
Only the Admin will have the authority to delete personnel. Inactive personnel cannot log into the system.
Anyone logged in can read and list the departments, but only the Admin can perform CUD operations.
We will use token authentication. When a user logs out, the token will be deleted. Token operations will be performed only by the Admin.
