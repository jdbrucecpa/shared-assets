# Shared Assets Repository

This repository hosts shared assets across multiple projects, including:

- **Email Templates** - HTML email templates for authentication flows
- **Static Assets** - Images, fonts, and other shared resources
- **Configuration Files** - Shared configuration templates

## Email Templates

Production-ready HTML email templates for Supabase authentication:

### Available Templates

- `email-templates/magic-link.html` - Magic Link authentication
- `email-templates/confirmation.html` - Email verification  
- `email-templates/recovery.html` - Password recovery
- `email-templates/email-change.html` - Email change confirmation
- `email-templates/invite.html` - Team invitations

### Template Variables

Templates support standard Supabase variables:
- `{{ .SiteURL }}` - Application URL
- `{{ .TokenHash }}` - Authentication token
- `{{ .Email }}` - User email address
- `{{ .Data.user_type }}` - User type (candidate/employer/admin)

### Usage

Configure in Supabase GoTrue environment variables:

```bash
GOTRUE_MAILER_TEMPLATES_MAGIC_LINK=https://jdbrucecpa.github.io/shared-assets/email-templates/magic-link.html
GOTRUE_MAILER_TEMPLATES_CONFIRMATION=https://jdbrucecpa.github.io/shared-assets/email-templates/confirmation.html
GOTRUE_MAILER_TEMPLATES_RECOVERY=https://jdbrucecpa.github.io/shared-assets/email-templates/recovery.html
```

## Deployment

This repository is automatically deployed to GitHub Pages at:
https://jdbrucecpa.github.io/shared-assets/

Updates are live within minutes of pushing to the main branch.

## Contributing

1. Edit templates in the appropriate directories
2. Test templates locally
3. Commit and push changes
4. Templates are automatically deployed via GitHub Pages

---

© 2025 JD Bruce. All rights reserved.
