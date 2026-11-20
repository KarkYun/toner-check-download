## Configure Toner Check

Create a file named `.env.local` in the same folder as `TonerCheck.exe`. Paste the settings below, then launch Toner Check and open http://localhost:8080.

```dotenv
TONER_CHECK_ORIGIN=http://localhost:8080
TONER_CHECK_ADMIN_USERNAME=admin
TONER_CHECK_ADMIN_PASSWORD="replace-with-a-private-password"
TONER_CHECK_TEST_MODE=true
TONER_CHECK_PRINTER_NETWORKS=0.0.0.0/1,128.0.0.0/1
```

- `TONER_CHECK_TEST_MODE=true` starts a new local setup without sign-in. Manage sign-in from **Settings → Workspace access → Require sign-in**.
- The admin password is used for initial setup when sign-in is required and no admin account exists. Replace the placeholder with your own password.
- `TONER_CHECK_PRINTER_NETWORKS` allows public and private IPv4 printer addresses, excluding special addresses such as localhost. For office deployment, you can narrow it to specific printer IPs or subnets.

Keep `.env.local` on the host PC. Share this example in the README and keep real credentials out of GitHub.
