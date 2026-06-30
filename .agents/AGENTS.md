# Agent Runbook & Workspace Rules

This file is automatically loaded by Antigravity agents. It outlines the current project state, authentication details, and next engineering steps.

## Project: XPosts

A project to interact with X using AI agents, the Model Context Protocol (MCP), and the `xurl` CLI.

---

## 1. Current Progress & Engineering Context

### Authentication Setup (OAuth 2.0)
*   **App Status**: The project-level app **PostBot-Project-App** is created under the **PostBot** project in the X Developer Portal.
*   **Tier**: Enrolled in the **Free** tier (up to 1,500 posts/month).
*   **Credentials**: Stored locally in [.env](file:///Users/m5/Desktop/XPosts/.env) (which is ignored by Git in [.gitignore](file:///Users/m5/Desktop/XPosts/.gitignore)).
    *   *Note: Do NOT commit any credentials to this repo. They are stored in `.env` under `CLIENT_ID`, `CLIENT_SECRET`, `CONSUMER_KEY`, `CONSUMER_SECRET`, `ACCESS_TOKEN`, and `ACCESS_TOKEN_SECRET`.*
*   **Post History**:
    *   **First Post**: `2071781402782175652`
    *   **Second Post (Quote-Tweet)**: `2071781990961967213`

### Repository Files
*   [TERMS.md](file:///Users/m5/Desktop/XPosts/TERMS.md): Terms of Service (liability disclaimer).
*   [PRIVACY.md](file:///Users/m5/Desktop/XPosts/PRIVACY.md): Simple trust-based Privacy Policy.
*   [README.md](file:///Users/m5/Desktop/XPosts/README.md): Links to documents and repository description.
*   [.gitignore](file:///Users/m5/Desktop/XPosts/.gitignore): Configured to ignore [.env](file:///Users/m5/Desktop/XPosts/.env).

---

## 2. To-Do & Next Tasks

- [ ] **Set up a Remote Server**: 
    Currently, the application runs locally and uses a `localhost:8080` callback for OAuth 2.0 PKCE authentication. The task is to migrate or set up a remote server for this application.
    *   Update the redirect URI configuration in X Developer Portal to point to the remote server's callback endpoint.
    *   Build/deploy a server-side authentication handler that securely redirects the user and obtains/refreshes the OAuth tokens.
