# Contributions Guidelines

<!--toc:start-->
- [Contributions Guidelines](#contributions-guidelines)
  - [Contribution Process](#contribution-process)
    - [Version Control](#version-control)
    - [Creating Issues](#creating-issues)
    - [Pull Request Guidelines](#pull-request-guidelines)
    - [Commit Messages](#commit-messages)
    - [Branching](#branching)
      - [Branching Strategies](#branching-strategies)
      - [Branch Names](#branch-names)
    - [Reviews](#reviews)
      - [Purpose of Code Reviews](#purpose-of-code-reviews)
      - [Review Process](#review-process)
      - [How to Request a Review](#how-to-request-a-review)
        - [Review Etiquette](#review-etiquette)
    - [Clean Code](#clean-code)
      - [Documentation Comments](#documentation-comments)
      - [Comment Annotation Tags](#comment-annotation-tags)
<!--toc:end-->

## Contribution Process

To ensure a smooth and efficient contribution process within our team, please
follow these guidelines when contributing to any project:

### Version Control

We use Git for version control to manage our codebase effectively. If you need
to learn more about Git, please refer to the Git Documentation
[here][git docs].

Our Git Repositories are hosted over at [GitHub][spaxel-dev].

We expect from you a comprehensive understanding of GitHub, and what it offers.
Utilization of the whole platform is expected. May that be from using more
sophisticated tools (e.g. DevOps tools). Or down to productivity concepts such
as `Issues`, `Projects`, `Milestones`, `Discussions`, etc. which
we use for our Sprint Planning.

Using these productivity tools enhances collaboration among team members by
organizing discussions around specific issues, ensuring focused communication.
Project management is improved through `Projects` and `Milestones`, which help
structure work and track deadlines effectively. The visual representation
provided by `Projects` allows teams to monitor task status and identify
bottlenecks, facilitating better prioritization and resource allocation.

These tools also promote accountability, as team members can assign tasks and
set due dates, making responsibilities clear.

We encourage looking over the capabilities of GitHub, and familiarizing
yourself to the platform if you aren't already.

### Creating Issues

Before starting work on a new feature or bug fix, it’s important to create an
issue in the project repository. This helps track work and facilitates
communication among team members. When creating an issue, please follow these
guidelines:

- __Title__: Use a clear and descriptive title that summarizes the issue or
feature.

- __Description__: Provide a detailed description of the issue or feature
request, including:
  - Steps to reproduce (for bugs)
  - Expected behavior
  - Any relevant screenshots or logs

- __Labels__: Apply appropriate labels e.g. "bug", "feature", "enhancement")
categorize the issue.

- __Assignee__: Assign the issue to yourself or another team member who will be
responsible for addressing it.

These are just the bare bone requirements, and are usually provided by default
through our `Issues Templates`.

Through templates you will be asked to select the type of issue (e.g. feature,
bug, etc.), and from then on you are expected to fill the template accordingly.

---

### Pull Request Guidelines

When, you are ready to submit your changes, you will create a Pull Request
(PR). Follow these guidelines for creating PRs:

- __Title__: Use a clear and descriptive title that summarizes the changes
made.

- __Description__: Include a detailed description of the changes, referencing
the related issue number (e.g. "Fixes #123", "Closes #123", etc.) and
explaining the rationale behind the changes.

- __Reviewers__: Assign team members to review your PR. Ensure that at least
one reviewer is assigned before merging.

- __Checklists__: Include a checklist in the PR description to confirm that you
have completed necessary tasks (e.g. "Code reviewed", "Tests added",
"Documentation updated").

Just like with [Issues](#creating-issues), these are the fundamental
requirements. Templates are provided with pull requests as well.

---

### Commit Messages

We follow a semantic commit message convention to maintain clarity in our
project history. When committing changes, please adhere to the following
format:

```plaintext
<type>(<scope>): <subject>

<body>
```

- __Type__: Specify the type of change (e.g. `feat` for new features, `fix` for
bug fixes, `docs` for documentation changes, etc.).

- __Scope__: (Optional) Indicate the scope of the change (e.g. a specific
module or component).

- __Subject__: Write a short summary of the change (max. 72 characters).

- __Body__: (Optional) Provide additional context or details about the change
(that don't fit into the max. 72 characters title limit).

For a comprehensive guide on how to structure your commit messages, please
refer to the [Conventional Commits Specification][semantic commit].

__Example Commit Message__:

```plaintext
feat(ui): add new button component

This commit introduces a new button component with customizable styles.
```

---

### Branching

To maintain a clear and organized workflow, we follow specific branching
strategies and naming conventions. This helps ensure that our codebase remains
manageable and that team members can easily navigate through branches.

#### Branching Strategies

Branching Strategies might depend on the project you're working, so always
consult the _README_ of that project. The most common strategy tends to be
[Gitflow][gitflow ref]

#### Branch Names

Just like with git messages, for branches, we adhere to the following format.

```plaintext
<type>/<description>
```

- __Type__: This indicates the purpose of the branch. Common types include:
  - feat: For new features or enhancements
  (e.g. `feat/add-user-authentication`).
  - fix: For fixing bugs (e.g. `fix/login-error`).
  - release: For preparing a new release (e.g. `release/1.0.0`).
  - etc.

- __Description__: A brief, descriptive name that summarizes the purpose of the
branch. Use hyphens to separate words for better readability.

When it comes to branch naming, conventions can be more relaxed for that
manner, as long as they follow the [Conventional Commits Specification]
[semantic commit] (adapted for branches like above), or are clear enough.
However, to maintain clarity and consistency, please follow these naming
conventions for branches:

- Use lowercase letters for branch names.
- Separate words with hyphens (-) for readability.
- Keep the description concise but descriptive enough to understand the purpose
of the branch.

By following these branching strategies and naming conventions, we can ensure a
more organized and efficient workflow, making it easier for team members to
collaborate and manage the codebase effectively.

### Reviews

#### Purpose of Code Reviews

Code reviews are an essential part of our development process. They help ensure
code quality, maintainability, and adherence to project standards. They also
provide an opportunity for knowledge sharing among team members.

#### Review Process

When you submit a pull request (PR), it will be reviewed by at least one other
team member.

Reviewers will check for:

- Code correctness and functionality
- Adherence to coding standards and best practices
- Clarity and readability of the code
- Adequate test coverage
- Proper documentation and comments

#### How to Request a Review

After pushing your changes, reviewers should be automatically assigned to your
PR (through the [`CODEOWNERS`][CODEOWNERS] file).

If the repository you're working in happens to not have a `CODEOWNERS` file, when
you create a PR, you can assign the relevant reviewers.

Alternatively, if you need a prompt review, you can
post the PR in our [`#tech-code-review`][review channel] Slack channel, tagging
the relevant reviewers.

##### Review Etiquette

- Be respectful and constructive in your feedback.
- Focus on the code, not the person.
- If you disagree with a suggestion, discuss it openly and provide reasoning
for your perspective.
- Address feedback promptly and make necessary changes to your code.

If you have questions or need clarification on feedback, don’t hesitate to ask.

### Clean Code

#### Documentation Comments

It is expected from you to decorate program constructs (methods, classes,
enums, etc.) with documentation comments specific to the language in use. This
helps establish a natural API reference directly in the codebase, allowing team
members to navigate and comprehend the code more efficiently. As a valuable
byproduct, this also enables modern code editors and IDEs equipped with
intelligent tooling (such as LSPs, IntelliSense, etc.) to infer these comments
and provide inline information within the method signatures.

__Example (JavaScript):__

```js
// NOTE: JSDoc
/**
 * Represents a person.
 * @class
 */
class Person {
    /**
     * Creates a person.
     * @param {string} name - The name of the person.
     * @param {number} age - The age of the person.
     */
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    /**
     * Greets the person.
     * @returns {string} A greeting message.
     */
    greet() {
        return `Hello, my name is ${this.name}.`;
    }
}
```

__Example (Python):__

```py
class Person:
    """
    Represents a person.

    Attributes:
    name (str): The name of the person.
    age (int): The age of the person.
    """

    def __init__(self, name, age):
        """
        Creates a person.

        Parameters:
        name (str): The name of the person.
        age (int): The age of the person.
        """
        self.name = name
        self.age = age

    def greet(self):
        """
        Greets the person.

        Returns:
        str: A greeting message.
        """
        return f"Hello, my name is {self.name}."
```

#### Comment Annotation Tags

For additional code clarity and effective collaboration, we encourage the use
of the following comment annotation tags in your contributions. These tags
should be used judiciously to provide meaningful insights and are not meant to
replace [Issues](#creating-issues).

- __NOTE__: Use this tag to explain the rationale behind specific
implementations or decisions. This helps others understand the context and
reasoning, especially in complex areas of the code. Example:

```py
# search.py
# NOTE: This algorithm uses a greedy approach for efficiency.
```

- __TODO__: Reserve this tag for tasks that need to be addressed in the future,
such as enhancements or additional features. It’s a way to highlight work that
is planned but not yet completed, ensuring it’s not forgotten. Example:

```js
// auth.js
// TODO: Add unit tests for this function.
```

- __WARN__: This tag should be used to indicate potential issues or deprecated
features that may affect the code's functionality. It serves as a caution for
others who may work on or use the code later. Example:

```cs
// Call.cs
/*
 * WARN: This API will be deprecated in the next version.
 * Plan migration accordingly.
 */
```

- __FIXME__: Use this tag to mark known issues that require resolution. This
helps maintain a clear record of outstanding problems that need attention.
Example:

```lua
-- plugin.lua
-- FIXME: This function fails with null input; needs validation.
```

<!-- ## Sprint Planning -->

<!--
TODO: Darius covers this: Perhaps adding a bit about Agile, and then the
strategy we'll cover for sprint planning.
-->

[git docs]: https://git-scm.com/doc
[spaxel-dev]: https://github.com/spaxel-dev
[semantic commit]: https://www.conventionalcommits.org/en/v1.0.0/#specification
[gitflow ref]: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
[CODEOWNERS]: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners
[review channel]: https://spaxel.slack.com/archives/C05S054TCBC
