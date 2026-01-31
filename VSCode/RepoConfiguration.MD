The error you're seeing is due to GitHub deprecating password authentication for Git operations. You need to use a **personal access token (PAT)** instead of your password.

Here's how to fix it:

1. **Create a Personal Access Token (PAT):**
   - Go to [GitHub Developer Settings](https://github.com/settings/tokens)
   - Click "Generate new token"
   - Select the appropriate scopes (e.g., `repo` for full access)
   - Generate the token and copy it

2. **Use the Token Instead of Your Password:**
   - When prompted for a password during `git push`, paste your PAT
   - You can also configure Git to store your token securely using the credential helper:
     ```bash
     git config --global credential.helper store
     ```
   - Then run `git push` again and enter your username and token when prompted

3. **Alternative: Use SSH Instead of HTTPS**
   - Generate an SSH key and add it to your GitHub account
   - Change the remote URL to use SSH:
     ```bash
     git remote set-url origin git@github.com:bmcgaugh/ai-prompts.git
     ```

This should resolve the authentication issue.
