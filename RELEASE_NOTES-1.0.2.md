## 🚀 Release Notes

---

### 🎉 New GitHub Actions

In this release, we've introduced 3 new GitHub actions to streamline the CI/CD process. Here are the details:

#### 1. **SSH Setup**

- **Description**: Handles the setup of SSH keys.
- **Inputs**:
  - `ssh-private-key`: Private SSH Key (Required).
  - `ssh-known-hosts`: SSH Known Hosts (Required).
  
- **Main Features**:
  - Creates the necessary SSH directories and files in the environment.
  - Sets correct permissions for the SSH key and known hosts.

---

#### 2. **Ansible Lint Action**

- **Description**: Lints an Ansible playbook using `ansible-lint`.
- **Inputs**:
  - `playbook`: Path to the Ansible playbook to be linted (Defaults to `main.yaml`).
  
- **Main Features**:
  - Checks out the repository code.
  - Sets up Python.
  - Installs `ansible-lint` and relevant galaxy collections.
  - Runs `ansible-lint` on the specified playbook.

---

#### 3. **Cache Procedure**

- **Description**: Handles caching based on the day and cache name.
- **Inputs**:
  - `cache-name`: Name for the cache, e.g., packages, pip, ansible-galaxy, etc. (Required).
  - `cache-id`: ID for cache, defaults to the current date (Optional).
  
- **Main Features**:
  - Determines the CACHE_ID based on the provided input or the current date.
  - Determines the cache path based on the operating system and input cache name.
  - Restores cache using the determined CACHE_ID.
  - Updates packages, pip, or installs ansible galaxy collections based on the cache name and hit status.

---

### 🔧 Instructions

To utilize these actions in your workflows:

1. Refer to the action using the appropriate path in your workflow `.yml` file.
2. Provide the necessary inputs as described above.
3. Adjust the actions' steps if necessary to fit into your CI/CD process.

---

⚠️ **Note**: Always review the action code and adjust as necessary for your specific use case and security requirements. 

---

🙏 Thank you for using these actions! Your feedback is always appreciated.
