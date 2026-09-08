# GitHub Upload Checklist

## Before Push

- [ ] Remove passwords/secrets
- [ ] Remove MFA QR codes/setup keys
- [ ] Remove access tokens/client secrets
- [ ] Redact personal email addresses where appropriate
- [ ] Redact unnecessary IP addresses
- [ ] Do not upload raw exported identity logs
- [ ] Add screenshots to `evidence/`
- [ ] Use descriptive screenshot filenames
- [ ] Review repository once before making it public

## Suggested Git Commands

```bash
git init
git add .
git commit -m "Add Microsoft Entra ID IAM lab"
git branch -M main
git remote add origin <YOUR-GITHUB-REPOSITORY-URL>
git push -u origin main
```

Replace `<YOUR-GITHUB-REPOSITORY-URL>` with your own GitHub repository URL.