# 🚀 PXBackup

### Automated VPS Backups. Simplified.

**PXBackup** is a modern VPS backup management platform designed to make server backups simple, secure, and automated. Connect remote servers through SSH, configure backup schedules, choose storage destinations, and manage everything from a beautiful, futuristic dashboard.

Built for developers, server administrators, and infrastructure enthusiasts who want reliable backups without unnecessary complexity.

---

## ✨ Features

- 🔐 **Secure Authentication** — Register and log in securely, with support for GitHub and Google OAuth.
- 🖥️ **VPS Management** — Connect and manage remote VPS servers through SSH.
- 📦 **Automated Backups** — Back up selected files and directories from remote servers.
- 🗓️ **Flexible Scheduling** — Schedule daily, weekly, or manual backups.
- ♻️ **Smart Backup Replacement** — Maintain one active backup per job, replacing it only after the new backup has been verified.
- ☁️ **Storage Destinations** — Configure supported storage providers for backup files.
- 📊 **Live Dashboard** — Monitor backup status, storage usage, schedules, and recent activity.
- 🛡️ **Security First** — Designed around encrypted credentials, access controls, and secure SSH connections.
- 🛠️ **Admin Panel** — Manage users, quotas, backup jobs, system settings, and application health.
- 📜 **Execution Logs** — Track backup progress, successful runs, and failures.
- 🎨 **Modern UI/UX** — A responsive interface with smooth animations and a premium dark theme.

---

## ♻️ Smart Backup Replacement

PXBackup follows a simple rule: **one active backup per backup job.**

For example:

1. Monday at 2:00 PM — PXBackup creates the first backup.
2. Tuesday at 2:00 PM — PXBackup creates and verifies a new backup.
3. After successful verification, the new backup replaces the previous one.
4. If the new backup fails, the previous successful backup is preserved.

This prevents old backup files from accumulating unnecessarily while protecting the last known-good backup.

Execution logs may be retained for monitoring and troubleshooting, but they are not additional backup copies.

---

## 🔑 Authentication

PXBackup is designed to support:

- Email and password authentication.
- GitHub OAuth.
- Google OAuth.
- Secure sessions and account management.
- Role-based access for users and administrators.

OAuth providers require valid client credentials and callback configuration.

---

## 🖥️ Server Management

Connect VPS servers using SSH credentials, including:

- Server IP address or hostname.
- SSH port.
- SSH username.
- SSH private key or password authentication.
- Optional private-key passphrase.

PXBackup should verify SSH host keys and protect stored credentials. Never expose private keys, passwords, or OAuth secrets in frontend code or public repositories.

---

## 🗓️ Backup Scheduling

Configure backup jobs to run automatically according to a preferred schedule.

Examples:

- Every day at 2:00 PM.
- Every Monday at 2:00 PM.
- Manual execution whenever needed.

Schedules should run independently of the user's browser session.

---

## 🛠️ Admin Panel

The administrative interface is designed to provide centralized control over:

- User accounts and permissions.
- Server and backup-job metadata.
- Account quotas and resource limits.
- Backup execution monitoring.
- Storage configuration.
- Scheduler and worker health.
- Global application settings.
- Audit logs and system activity.

Administrative actions must be authorized on the backend.

---

## 🧱 Technology Stack

The final technology stack depends on the selected implementation or existing repository.

A potential stack includes:

- **Frontend:** Next.js, React, TypeScript.
- **UI:** Tailwind CSS and shadcn/ui.
- **Animations:** Framer Motion.
- **Backend:** Server-side APIs and background workers.
- **Database:** PostgreSQL.
- **Authentication:** Auth.js or an equivalent authentication framework.
- **Scheduling:** A persistent scheduler and job queue.
- **Deployment:** Docker Compose.

These are proposed technologies, not a claim that every component has already been implemented.

---

## ⚙️ Configuration

Create an environment file based on the project's environment-variable example.

Typical configuration may include:

- `DATABASE_URL`
- `APP_URL`
- `AUTH_SECRET`
- `GITHUB_CLIENT_ID`
- `GITHUB_CLIENT_SECRET`
- `GOOGLE_CLIENT_ID`
- `GOOGLE_CLIENT_SECRET`

Additional configuration may be required for backup workers, encryption keys, and storage providers.

**Never commit real secrets or production environment files to GitHub.**

Refer to the project setup documentation for the actual variables and deployment instructions.

---

## 🚧 Project Status

PXBackup is a project for building a modern, secure, and reliable VPS backup management platform.

Features and integrations depend on the current implementation. Consult the repository documentation for completed functionality and setup requirements.

---

## 🔮 Vision

The goal of PXBackup is to make VPS backup management easier through automation, a clean user experience, reliable backup replacement, and centralized infrastructure management.

---

## 🤝 Contributing

Contributions, suggestions, bug reports, and feature ideas are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make the changes and test them.
4. Submit a pull request describing the improvements.

Please avoid submitting credentials, private keys, personal data, or production backup files.

---

## 📄 License

PXBackup is licensed under the [MIT License](LICENSE).

You are free to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, subject to the conditions of the MIT License.

See the [LICENSE](LICENSE) file for the full license text.

---

**PXBackup — Backups you can count on.** 🔐
