# Contributing to GoAtlas Book

Thank you for your interest in contributing to GoAtlas! This is a
community-driven book and every contribution matters — from fixing a
typo to writing an entire section.

---

## Table of Contents

- [Ways to Contribute](#ways-to-contribute)
- [Reporting Issues](#reporting-issues)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Writing Standards](#writing-standards)
- [Code of Conduct](#code-of-conduct)

---

## Ways to Contribute

You do not need to be a Go expert to contribute. Here are some ways
you can help:

- **Fix typos or grammar mistakes** — even small fixes are valuable
- **Improve explanations** — if something is confusing, it can be better
- **Fix technical errors** — wrong code, outdated syntax, incorrect output
- **Suggest new topics** — open an Issue with your suggestion
- **Add or improve code examples** — practical examples help a lot
- **Review open Pull Requests** — giving feedback is also contributing

---

## Reporting Issues

If you found an error, something confusing, or want to suggest a topic,
open an [Issue](../../issues) and follow these guidelines:

- **Use a clear and descriptive title**
- **Mention the chapter and section** where the problem is
- **Describe the problem** — what is wrong and why it is confusing
- **If it is a technical error**, include the correct version if you know it
- **If it is a suggestion**, explain why the topic would be useful

> ⚠️ Please search existing issues before opening a new one to avoid
> duplicates.

---

## Submitting a Pull Request

If you want to fix or improve something directly, follow these steps:

1. **Fork** this repository by clicking the _Fork_ button on GitHub
2. **Clone** your fork to your machine:
```bash
   git clone https://github.com/your-username/goatlas-book.git
```
3. **Create a new branch** with a descriptive name:
```bash
   git checkout -b fix/typo-introduction
```
4. **Make your changes** in the relevant Markdown files
5. **Commit** your changes with a clear message:
```bash
   git commit -m "fix: correct typo in introduction chapter"
```
6. **Push** to your fork:
```bash
   git push origin fix/typo-introduction
```
7. Open a **Pull Request** on GitHub and describe what you changed and why

> 💡 For large changes like new sections or chapters, please open an
> Issue first to discuss it before writing everything.

---

## Writing Standards

To keep the book consistent, please follow these guidelines:

**Language**
- The book is written in **Brazilian Portuguese**
- File and folder names must be in **English**
- Code, variables, and comments inside examples must be in **English**

**Tone**
- Write in a clear, friendly, and approachable way
- Avoid overly technical jargon without explanation
- Always explain the _why_, not just the _how_

**Code Examples**
- All examples must be valid and runnable Go code
- Use `go fmt` formatting standards
- Keep examples short and focused on the concept being explained
- Always show the expected output when relevant:

```go
  package main

  import "fmt"

  func main() {
      fmt.Println("Hello, GoAtlas!")
  }
  // Output: Hello, GoAtlas!
```

**Markdown Formatting**
- Use `#` for chapter titles, `##` for sections, `###` for subsections
- Use code blocks with the language specified (` ```go `)
- Keep lines under 80 characters when possible
- Leave one blank line between paragraphs

**Commit Messages**
Follow this pattern:
- `fix:` for corrections (typos, technical errors)
- `improve:` for improvements to existing content
- `add:` for new content
- `remove:` for removed content

Examples:
- fix: correct variable example in types section
- improve: rewrite goroutines explanation for clarity
- add: new section about defer keyword

---

## Code of Conduct

GoAtlas is an inclusive and welcoming project. We expect all
contributors to:

- Be respectful and considerate in all interactions
- Accept constructive feedback graciously
- Focus on what is best for the community and the readers
- Avoid discriminatory, offensive, or harmful language

Disrespectful behavior will not be tolerated and may result in being
blocked from the project.

---

If you have any questions, feel free to open an
[Issue](../../issues) or start a
[Discussion](../../discussions).

We are happy to help! 🚀
