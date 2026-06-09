# Version Control & Team Collaboration Notes

## Version Control

Version control is a system used to track changes in code and project files over time. It helps teams collaborate and manage application development efficiently.

### Common Tool

* Git

### Benefits

* Tracks code changes.
* Maintains version history.
* Supports collaboration.
* Allows rollback to previous versions.
* Prevents accidental code loss.

### Common Concepts

* Repository (Repo)
* Branch
* Commit
* Merge
* Pull Request

---

## Collaboration

Collaboration allows multiple developers to work on the same project without overwriting each other's work.

### Best Practices

* Work on separate branches.
* Pull latest changes before starting work.
* Review code before merging.
* Communicate changes with team members.
* Resolve conflicts carefully.

### Benefits

* Better code quality.
* Faster development.
* Knowledge sharing across teams.

---

## Commit Discipline

A commit should represent a meaningful and complete unit of work.

### Good Commit Practices

✅ Commit small, focused changes.

✅ Write clear commit messages.

✅ Test before committing.

✅ Commit frequently.

### Examples

Good:

```text
Add validation for Account creation
```

Good:

```text
Fix case assignment flow error
```

Poor:

```text
Changes
```

Poor:

```text
Updated stuff
```

### Benefits

* Easier troubleshooting.
* Better project history.
* Simpler code reviews.

---

## Team Workflow

A common team workflow using Git:

### Step 1: Pull Latest Changes

```text
Main Branch
    ↓
Developer pulls latest code
```

### Step 2: Create Feature Branch

```text
feature/account-validation
```

### Step 3: Develop and Test

* Build functionality.
* Run tests.
* Verify requirements.

### Step 4: Commit Changes

```text
Add account validation logic
```

### Step 5: Push Branch

* Upload changes to repository.

### Step 6: Create Pull Request

* Request code review.
* Address feedback.

### Step 7: Merge

* Merge approved code into the main branch.

### Team Workflow Diagram

```text
Main Branch
      ↓
Create Feature Branch
      ↓
Develop & Test
      ↓
Commit Changes
      ↓
Push Branch
      ↓
Pull Request
      ↓
Code Review
      ↓
Merge to Main
```

---

## Salesforce Team Workflow Example

1. Developer creates an LWC feature.
2. Apex logic is developed.
3. Changes are tested in Sandbox.
4. Code is committed to Git.
5. Pull Request is created.
6. Team reviews the code.
7. Changes are merged.
8. Deployment is performed.
9. Production is monitored.

---

## Quick Summary

| Topic             | Purpose                                         |
| ----------------- | ----------------------------------------------- |
| Version Control   | Track and manage code changes                   |
| Collaboration     | Enable multiple developers to work together     |
| Commit Discipline | Maintain clean and meaningful project history   |
| Team Workflow     | Standard process for development and deployment |

### Development Lifecycle

**Plan → Branch → Develop → Test → Commit → Review → Merge → Deploy → Monitor**.
