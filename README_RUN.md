Run project helper

This repository includes a convenience PowerShell script `run_project.ps1` to automate common local setup tasks.

Usage examples (PowerShell):

- Install deps, migrate, start server and open Edge:

  .\run_project.ps1 -OpenBrowser

- Install deps, migrate, seed the medicines, create a superuser and open browser:

  .\run_project.ps1 -Seed -CreateSuperuser -OpenBrowser

Notes:
- `CreateSuperuser` will prompt for username, email and a secure password.
- The script requires Python in PATH and will use `python` to run manage.py commands.
- For production-like email sending, set SMTP env vars as described in `pharmacy_project/settings.py`.
