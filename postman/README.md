## API Testing – Postman

This project includes a collection of API tests created in [Postman](https://www.postman.com/). The tests are designed for the `ManagMe` project backend (Express + MongoDB) and cover basic CRUD operations, authentication and token handling.

### Files

Inside the `/postman` directory you will find:

- `ManagMe.postman_collection.json` – the Postman collection containing all test requests and test scripts
- `ManagMe.postman_environment.json` – the environment file with variables like `DBurl`, `Expressurl`, and JWT tokens

---

### How to Use

#### 1. Import to Postman

1. Open [Postman](https://www.postman.com/)
2. Go to `File` → `Import`
3. Import both files:
   - Collection: `ManagMe.postman_collection.json`
   - Environment: `ManagMe.postman_environment.json`

#### 2. Set Environment

In the top right corner of Postman, select the imported environment named `ManagMe`.

#### 3. Run Tests

You can:
- Manually send requests from the collection
- Or use the **Collection Runner**:
  1. Click the `ManagMe` collection → `Run Collection`
  2. Choose the environment
  3. Click `Run`

#### 4. Token Handling

- After sending the `Login-admin` request, the script automatically saves `token` and `refreshToken` to the environment.
- These tokens are then used in requests that require authorization.

---

### Covered Endpoints

| Endpoint | Method | Description |
|------------------------|--------|-------------------------|
| `/token` | POST | Login – sets tokens |
| `/refreshToken`| POST | Refresh JWT |
| `/protected` | GET| Get user data (auth) |
| `/projects` | GET| Get all projects |
| `/projects/:id` | GET| Get project by ID |
| `/projects` | POST | Create project |
| `/projects/:id` | PUT | Edit project |
| `/projects/:id` | DELETE | Delete project |

---

### Tools & Concepts Used

- Status code assertions (`pm.test(...)`)
- Response field validation (`pm.expect(...)`)
- Response status check (`pm.response.to.have.status(...)`)
- Token management in environment
- Dynamic environment variable usage (`{{DBurl}}`, `{{token}}`, etc.)

### Sample Test Run Result

Below is an example of a test run result using the Postman Collection Runner:

[Test Run Result](screenshots/test-run-results-1.png)
[Test Run Result](screenshots/test-run-results-2.png)