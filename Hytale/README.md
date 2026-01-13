# Hytale Server Template

This template installs and runs a Hytale dedicated server in PufferPanel. Just fill out the variables during setup and press install, the server will automatically download and configure everything needed to run.

---

## Authentication (Required)

Hytale servers must be authenticated before they will accept players. This is **standard behavior for all Hytale servers**, regardless of hosting method or control panel, and is not specific to this template.

---

## Setup Steps

### 1. install

During installation, you will get told to authenticate with a link, do this.

---

### 2. Authenticate the server again

After the server has installed, start it.

Run the following command:

```
auth login device
```

Follow the on-screen instructions to authenticate.

---

### 3. Make authentication permanent

To keep the server authenticated permanently, run:

```
auth persistence Encrypted
```

---

### 4. Final restart

Restart the server one final time. Your server is now permanently authenticated and ready for players.

---

If the server does not allow connections, re-check that the authentication steps were completed in the correct order and that all template variables were filled in correctly.
