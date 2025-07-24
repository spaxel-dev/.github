## 📝 Summary

Briefly describe what this PR does and why it’s needed.

Example:
> This PR refactors the authentication flow to support OAuth 2.0 login while preserving backward compatibility.

---

## 🔍 What Changed

- Introduced new middleware for handling token refresh
- Updated `AuthContext` to reflect new user roles
- Removed deprecated cookie-based login logic

---

## 🔗 Related Issue(s)

> [!IMPORTANT]
> Always ensure that you have an existing issue for this respective PR to link with.

Closes #[ISSUE_NUMBER]
Refs #[ISSUE_NUMBER]

---

## ✅ Checklist

- [ ] I’ve tested this locally or in staging
- [ ] I’ve updated documentation (if needed)
- [ ] I’ve linked relevant issues or discussions
- [ ] This is a small, focused change (single concern)
- [ ] I’ve followed our [Contribution Guidelines][contributing]

---

## 💬 Additional Context

Add any other information, screenshots, or notes for reviewers here.

---

## 🧪 How to Test

Provide steps for others to verify your changes:

```sh
# Example
npm run test
npm run dev
```

[contributing]: https://github.com/spaxel-dev/.github-private/blob/main/profile/CONTRIBUTING.md
