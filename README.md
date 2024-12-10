# Postman API Automation with Newman and GitHub Actions

This project is all about automating API testing using **Postman**, **Newman**, and **GitHub Actions**. It includes a set of **11 test cases** designed to validate the functionality of a mock API. One of the key takeaways from this project is learning how to make quick changes to test cases directly in the exported Postman collection file without the need to re-export every time. It’s a practical and efficient way to handle API testing.

---

## Features

- **Mock API Testing**: A Postman collection with multiple test cases to validate endpoints for various scenarios, both positive and negative.
- **Automation with GitHub Actions**: Automatically runs tests every time a change is pushed to the repository.
- **Direct Test Editing**: Test cases can be updated directly in the exported JSON file to save time and effort.
- **Reports**: Test results clearly show what passed and what failed, making it easy to debug.

---

## What’s Special About This Project

I made a change to one of the test cases directly in the Postman collection file instead of going through Postman. Here’s what I did:

- I removed Test Case **TC-11**, which was checking for invalid JSON syntax.
- After removing it, I updated the numbering of the remaining test cases so everything stayed consistent.

This showed how you can skip re-exporting files from Postman when making changes, saving time and effort. This approach might seem small, but it’s incredibly useful when working with API automation.

---

## How GitHub Actions Fits In

To keep things automated, I set up a GitHub Actions workflow (`newman.yml`) that does the following:

- Runs tests automatically whenever code is pushed to the repository.
- Uses a Linux environment (**ubuntu-latest**) to execute the tests.
- Installs Newman, runs the Postman collection, and generates test reports.
- Outputs clear results, showing which tests passed and which failed.

This setup makes it easy to catch issues early and ensures consistent test execution every time.

---

## Prerequisites

- Postman installed on your local machine.
- Newman installed globally (`npm install -g newman`).
- A GitHub account with a repository for this project.
- **VS Code** or any IDE of your choice.

---

## Getting Started

Here’s how you can get this project up and running:

### 1. Clone the Repository
Start by cloning the repository to your local machine

```bash
git clone https://github.com/your-username/postman-api-automation.git
cd postman-api-automation
```

## 2. Install Newman
Make sure you have Node.js installed, then install Newman.

```bash
npm install -g newman
```

## 3. Run the Tests Locally
You can test the Postman collection locally using Newman.

```bash
newman run postman_collection.json
```

## 4. Automate with GitHub Actions
Once you’ve made changes and pushed them to GitHub, the workflow will automatically run the tests for you. Just check the **Actions** tab in GitHub to see the results.


## 5. Review Test Results
Results are visible in the **GitHub Actions** tab. 
Alternatively, generate local reports using:

```bash
 newman run postman_collection.json --reporters cli,json --reporter-json-export results.json
 ```


## How You Can Learn from This Project
This project is great if you’re looking to:

- Understand how to test APIs using Postman and Newman.
- Set up CI/CD pipelines for API testing with GitHub Actions.
- Edit Postman test cases directly in the JSON file, which can be faster and more efficient for certain tasks.

## Contributing
Feel free to fork this repository and contribute to the project by submitting pull requests.

## License
This project is licensed under the **MIT License**. Check the **LICENSE** file for more details.
You are free to use, modify, and distribute this project as per the license terms.

  