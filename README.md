# 🔍 Git Internals Lab

A hands-on exploration of how Git works under the hood. This project dives into the mechanics of Git's object storage, commit structures, and repository internals.

## About

Ever wondered what actually happens when you run `git commit`? This lab helps you understand Git's internal architecture by examining real object stores, exploring tree structures, and tracing through commits.

Perfect for developers who want to move beyond basic Git commands and truly understand how the most important tool in modern software development actually works.

## What's Inside

- **Live Git Objects**: Explore actual Git object files in the `.git/objects` directory
- **Commit Analysis**: Trace commits and understand their structure
- **Tree Exploration**: See how Git represents your project's file structure
- **Learning Examples**: Simple, real examples to study Git internals

## Getting Started

### Prerequisites

- Git installed on your system
- A terminal (PowerShell, Bash, etc.)
- Basic familiarity with Git commands

### Quick Start

1. **Explore Git objects:**
   ```powershell
   Get-ChildItem -Path .git\objects -File -Recurse
   ```

2. **View the current commit's tree:**
   ```bash
   git rev-parse HEAD^{tree}
   ```

3. **Inspect commit history:**
   ```bash
   git log --oneline --decorate --graph --all
   ```

## Common Git Internals Commands

### Count your objects
```bash
find .git/objects -type f | wc -l
```

### Inspect an object
```bash
git cat-file -p <object-sha>
```

### See what's in a commit
```bash
git rev-parse HEAD^{commit}
git rev-parse HEAD^{tree}
```

### View the object database stats
```bash
git count-objects -v
```

## Project Structure

```
git-internals-lab/
├── .git/                 # The magic happens here
│   └── objects/          # Git's object database
├── hello.txt             # Sample project file
└── README.md             # This file
```

## Learning Resources

- **Git Internals**: Study the `.git/objects` directory structure
- **Object Types**: Understand blobs, trees, commits, and tags
- **File History**: Trace how changes are stored as objects

## Tips for Exploration

1. Make changes to files and run `git add` to see new blob objects appear
2. Create commits and observe how tree and commit objects relate
3. Use `git cat-file -t` to identify object types
4. Use `git cat-file -p` to read object contents in human-readable form

## Want to Learn More?

- [Pro Git Book](https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain)
- [Git from the Inside Out](https://codewords.recurse.com/issues/two/git-from-the-inside-out)
- [Git Documentation](https://git-scm.com/doc)

---

**Happy exploring!** 🚀
