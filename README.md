# CI/CD Flow Templates

[![GitHub license](https://img.shields.io/github/license/bbaskovc/cicd)](https://github.com/bbaskovc/cicd/blob/feature/organise-project/LICENSE.md)
[![GitHub stars](https://img.shields.io/github/stars/bbaskovc/cicd-flow-templates)](https://github.com/bbaskovc/cicd/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/bbaskovc/cicd)](https://github.com/bbaskovc/cicd/network)
[![GitHub issues](https://img.shields.io/github/issues/bbaskovc/cicd)](https://github.com/bbaskovc/cicd/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/bbaskovc/cicd)](https://github.com/bbaskovc/cicd/pulls)



Welcome to the CI/CD Flow Templates repository! This repository contains a collection of reusable CI/CD (Continuous Integration/Continuous Deployment) templates designed to streamline your development workflow. Whether you're setting up a new project or optimizing an existing one, these templates can help you get started quickly and efficiently.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
  - [Using as a Git Template](#using-as-a-git-template)
  - [Using as a GitHub Action Workflow](#using-as-a-github-action-workflow)
  - [Copying into Your Project](#copying-into-your-project)
- [Contributing](#contributing)
- [License](#license)

## Introduction

CI/CD pipelines are essential for modern software development, enabling automated testing, building, and deployment processes. This repository provides a set of templates that you can customize to fit your project's needs, ensuring consistency and reliability in your development workflow.

## Features

- **Multi-Platform Support**: Templates for various CI/CD platforms like GitHub Actions, GitLab CI, Jenkins, and more.
- **Customizable**: Easily adaptable to fit different project structures and requirements.
- **Best Practices**: Incorporates industry best practices for CI/CD pipelines.
- **Documentation**: Clear and concise documentation to help you understand and use the templates effectively.

## Getting Started

To get started with the CI/CD flow templates, follow these steps:

1. **Clone the Repository**:

   git clone https://github.com/bbaskovc/cicd.git
   cd cicd-flow-templates

## Usage

### Using as a Git Template

You can use this repository as a template for your own repository. This allows you to start a new project with the CI/CD templates already in place.

1. Click the "Use this template" button on the GitHub repository page.
2. Follow the prompts to create a new repository based on this template.

### Using as a GitHub Action Workflow

You can directly use the workflows from this repository in your own GitHub Actions setup. Here's an example of how to do this:

1. Create a workflow file in your project, e.g., .github/workflows/ctest.yml.

2. Define the workflow to use the template from this repository:

   name: Run ctest check

   on:
     push:
       branches:
         - test/ctest

   jobs:
     ctest:
       uses: [bbaskovc/cicd/templates/github/ctest.yml](https://github.com/bbaskovc/cicd/blob/main/templates/github/ctest.yml)@main
       with:
         test_dir: 'tests/ctest'
         project_name: 'my_project_ctest'

3. Customize the with parameters as needed for your project.

### Copying into Your Project

If you prefer to copy the templates into your project manually, follow these steps:

1. Browse the available templates in the templates directory and select the one that best fits your project.

2. Copy the template file to your project's CI/CD configuration directory (e.g., .github/workflows for GitHub Actions).

3. Customize the template to match your project's specific requirements. Update paths, environment variables, and other configuration settings as needed.

## Contributing

Contributions are welcome! If you have a template or improvement to share, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with descriptive messages.
4. Push your branch to your fork.
5. Create a pull request to the develop repository.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE.md) file for details.

---

Thank you for using the CI/CD Flow Templates repository! We hope these templates help you streamline your development workflow and improve your project's reliability. If you have any questions or need further assistance, feel free to open an issue or reach out to the maintainers.

Happy coding! 🚀
