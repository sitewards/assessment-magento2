![Y1 Digital AG](./y1.logo.png)
=======

Assessment test to evaluate skills of Magento Backend Developer candidates.

# Credits

This is heavily based on https://github.com/vissimo-group/assessment-magento2

# Introdution

This assessment test aims to assessing your knowledge as a Magento Backend developer. The assessment test will assess your skills on:

- Your level of knowledge of the PHP OOP language (PHP version 7.4+)
- Magento component architecture (Magento Open Source/Commerce 2.4+);
- Knowledge of the main design patterns used by the platform
- Use of dependency injection
- Magento Plugins (Interceptors)
- Code standards and good programming practices
- SOLID Principles and PHP Standards Recommendations (PSR)
- Composer

# What will be evaluated?

- Structure and organization of code and files
- Adopted solutions
- Technologies used
- Quality
- PSR Patterns, Design Patterns
- Provided documentation and git history
- Anyway, everything will be observed and taken into consideration

# How to publish your test?

- Create a private repository on GitHub
- Follow all the instructions for running the assessment test
- When finished, invite the GitHub user **aboritskiy** to access your repository and evaluate your assessment test, see
  (https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository)

# Instructions

The main focus of our assessment test is to evalute your skills and knowledge as a Magento Backend developer.

You have complete freedom to increase some knowledge that you find interesting to apply in the evaluation.

> There is no problem if you are unable to run all the features of the assessment, do as much as you can.

## Basic features

 1. Module to create manufacturer entities and associate them with products;
 2. Use interfaces to create service contracts;
 3. The module must have resources to create, edit, list and delete manufacturers from Magento admin area;
 4. The module access must be available in the Magento Admin area through the 'Content > Manufacturers' menu;
 5. It should be possible to restrict access to Magento Admin users to create, edit, delete and list manufacturers;
 6. The manufacturer registration form must have:

| Field name       | Type        | Required | Additional checks                |
|------------------|-------------|----------|----------------------------------|
| Enable           | bool/UI toogle | Yes      |                                  |
| Name             | text        | Yes      | alphanumeric, max 150 characters |
| Description      | textarea    | No       | max 600 characters               |
| Producer Image   | file/UI     | Yes      | PNG or JPG                       |
| Producer Website | text        | No       | Valid URL                        |

 7. Set up a dropdown product attribute to select the manufacturer by name when creating a new product at Magento admin area;
 8. The product attribute must be created/modified through the module's setup, and it must be possible to remove it when uninstalling the manufacturer module
 9. The dropdown product attribute must list only manufacturer entities that have the `Enable = true`
 10. The product attribute must be available to layered navigation filtering
 11. Translation for all labels and texts with i18n

## Advanced features

These additional requirements are a differential and will have greater weight in relation to another candidates

 1. Import manufacturers from CSV file using MAGENTO CLI command;
 2. Make the manufacturer product attribute available in the GraphQl search at products query and aggregations;
 3. Add REST API Endpoint to manage manufacturer entities;
 3. All code must pass in Magento Static tests (Magento Coding standards);
 4. Create unit tests to cover at last 50% of classes;
 5. Create integration tests to cover:
	 - Test manufacturer create, list, edit and delete;
	 - Test product creation with manufacturer attribute;
 6. MFTF to tests all Magento admin area implementations for Producer Module
