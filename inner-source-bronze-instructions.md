# Inner Source Bronze Instructions

The following instructions are designed to ensure your repository is compliant with the Inner Source Bronze level requirements. Please follow these steps carefully:

1. Readme
    - Ensure your repository has a `README.md` in file in the root directory.
        - The `README.md` should include:
            - It should provide a high level description of the entire repository. Use the code and comments in the repository to help you write this.
            - Describe the primary functionality of the project

2. License
    - Include a `LICENSE` file in the root directory. 
    - If no specific license is specified, use [LICENSE](/templates/LICENSE)

3. Code of Conduct
    - Include a `CODE_OF_CONDUCT.md` file in the root directory.
    - Use the template from [CODE_OF_CONDUCT](/templates/CODE_OF_CONDUCT.md)

4. Contribution
    - Include a `CONTRIBUTION.md` file in the root directory.
    - Use the template from [CONTRIBUTION](/templates/CONTRIBUTION.md). Populate the template with the following sections:
        - Contribution Overview
        - Contribution Model - provide a high-level contribution process and steps for contributing
        - Moderation and Maintainer - use the PR Approvers to populate this list if maintainers are not yet defined. If that is not available get the list of committers to the main branch using the command `git log main --pretty=format:"%an <%ae>" | sort | uniq`. 
        - Quality Management details

5. Folder structure
    - Ensure the following folder structure is present:
        - `src/` - Contains the source code of the project.
        - `tests/` - Contains unit tests for the project.
        - `docs/` - Contains documentation files.
        - `scripts/` - Contains scripts for building, testing, or deploying the project.

6. SonarQube
    - Ensure the project is configured to use SonarQube for code quality analysis.
    - Include a `sonar-project.properties` file in the root directory with the necessary configuration that matches the requirements of the reopository and remove sections not needed. Ask the user for the SonarQube project key and other relevant details and populate them accordingly in the file.
    - Include a link to the SonarQube dashboard in the `README.md` file and add a badge to the README that shows the current quality gate status.
    - Ensure that the SonarQube analysis is run as part of the CI/CD pipeline. If the existing Github Actions workflows do not already run sonarqube scans, add the [SonarQube Github Action](templates/build.yml) to the `.github/workflows` directory.

7. Issue Template
    - Ensure the repository has an issue template for bug reports and feature requests.
    - Use the template from [ISSUE_TEMPLATE](/templates/issue_template.yml) if the repository does not have an issue template and place it in the `.github/ISSUE_TEMPLATE` directory.

8. Feature Request Template
    - Ensure the repository has a feature request template.
    - Use the template from [FEATURE_TEMPLATE](/templates/feature_template.yml) if the repository does not have a feature request template and place it in the `.github/ISSUE_TEMPLATE` directory.

