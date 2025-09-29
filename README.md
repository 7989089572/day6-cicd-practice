# 📘 Day 6 – Agile & CI/CD Practice

## 🚀 Topics Covered
1. Agile Methodology Fundamentals  
   - Agile values & principles  
   - Scrum roles & ceremonies  
   - Writing user stories & sprint planning  
   - Daily stand-up simulation  

2. Continuous Integration & Development (CI/CD)  
   - Basics of CI, CD, and Continuous Deployment  
   - Tools overview: Jenkins, GitHub Actions, GitLab CI/CD, AWS CodePipeline  
   - Setting up a GitHub Actions Workflow  

---

## 📝 Practice Work

### Agile User Stories (E-commerce Example)
- As a customer, I want to add products to the cart so that I can buy multiple items at once.  
- As a user, I want to track my order status so that I know when my package will arrive.  
- As an admin, I want to manage product inventory so that the website always shows available stock.  

### Sprint Breakdown
- Task 1: Design Add-to-Cart UI  
- Task 2: Implement backend API  
- Task 3: Write test cases  

### Daily Stand-up Simulation
- Yesterday: Learned Agile fundamentals  
- Today: Practiced user stories & CI/CD pipeline setup  
- Blockers: None 🚀  

---

## ⚙️ CI/CD Practice
- Created a `hello.py` program  
- Added GitHub Actions workflow (`ci.yml`) to run tests automatically on each push  

```yaml
name: CI Pipeline
on:
  push:
    branches: [ "main" ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v4
        with:
          python-version: '3.10'
      - run: pip install pytest
      - run: pytest
