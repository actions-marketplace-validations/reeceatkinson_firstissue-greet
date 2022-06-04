# Issue Review Greeter
This GitHub action allows you to make contributors aware that you have recieved the issue and to hold tight for a review by someone.

### Installation:
Copy and paste the following snippet into your .yml file.

```
- name: First Issue Greeting
  uses: reeceatkinson/issuereview-greet@v0.0.2-alpha
```

```
on: [issues]

jobs:
  greeting:
    runs-on: ubuntu-latest
    permissions:
      issues: write
    steps:
    - uses: actions/first-interaction@v1
      with:
        repo-token: ${{ secrets.GITHUB_TOKEN }}
        issue-message: 'Hi, thanks for taking the time to submit a issue. Great first issue!'
```

### Website
You can also find the README.md at https://reeceatkinson.github.io/firstissue-greet/
