# Contributing to Streaming Tech LTD Go Project

Thank you for your interest in contributing! By participating in this project, you agree to abide by the following guidelines.

---

## 1. Sign the Contributor License Agreement (CLA)

Before we can accept your contribution, you must sign our CLA. You can find it here:

- **[CLA.md](./CLA.md)**

_We will not merge any merge request (MR) until we have a signed CLA on file._

---

## 2. Developer Certificate of Origin (DCO)

Every commit you submit must include a “Signed-off-by” line. You can do this automatically with:

```bash
git commit -s -m "A concise, descriptive commit message"
```

This adds a line like:

```
Signed-off-by: Jane Contributor <jane@example.com>
```

which certifies that you have the right to contribute and agree to the CLA.

---

## 3. How to Contribute

1. **Fork** the repository (if you’re external) or create a **feature branch** off of `main`:
   ```bash
   git checkout -b feature/my-new-feature
   ```
2. **Make your changes** in Go.
3. **Run tests** (if any) and ensure everything passes.
4. **Commit** your work with clear messages and DCO sign-off:
   ```bash
   git commit -s -m "Add XYZ functionality"
   ```
5. **Push** your branch:
   ```bash
   git push origin feature/my-new-feature
   ```
6. **Open a Merge Request** against `main`, choosing the “feature/my-new-feature” branch.

---

## 4. Merge Request Checklist

- [ ] You’ve signed the CLA (CLA.md)
- [ ] All commits have `Signed-off-by:` lines
- [ ] CI builds are passing
- [ ] MR description clearly explains **what** and **why**
- [ ] You’ve added or updated tests/documentation as needed

---

## 5. Review Process

- MRs will be reviewed by the core maintainers.
- We may request changes—please respond promptly.
- Once approved and CI is green, a maintainer will merge your MR.

---

## 6. Questions & Support

If you’re unsure about anything, feel free to:

- Open an issue describing your question or problem
- Join our Discord chat (link in the [README](./README.md))
