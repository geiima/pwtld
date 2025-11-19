# Playwright Project: Faker.js & Secrets

This project demonstrates automated testing using **Playwright**, focusing on external library integration (`Faker.js`), environment variables, and Continuous Integration (CI) with **GitHub Actions**.

---

## 🛠️ Project Setup and Execution

### 1. How to Install Dependencies

To set up the project and install all required Node.js packages (including Playwright and Faker.js), run the following command in the project root:

    npm install

### 2. How to Run Tests

To execute the entire test suite locally:

    npx playwright test

### 3. How to Use Environment Variables

The application's base URL is retrieved from the **`APP_URL`** environment variable, ensuring the project remains flexible and secure.

- **Local Execution:** The value is read from a local **`.env`** file (e.g., `APP_URL=https://fe-delivery.tallinn-learning.ee/signin`).
- **CI Execution:** The value is securely read from a **GitHub Secret** named `APP_URL`.

The URL is accessed in the code using:

    await page.goto(process.env.APP_URL);

---

## ✨ Note on Data Generation

This project uses **Faker.js** to generate unique usernames and passwords for each test run, ensuring **test independence** and simulating real user behavior.
