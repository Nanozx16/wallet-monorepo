# wallet-monorepo

Key components
apps/: Contains application projects (e.g., mobile for the Safe{Wallet} mobile app).
packages/: Shared libraries and utilities.
config/: Configuration files for the monorepo.
Getting started
To get started, ensure you have the required tools installed and follow these steps:

Prerequisites
Node.js: Install the latest stable version from Node.js.
Yarn: Use Yarn version 4.5.3 or later
to install it with the latest node version you can simply do

corepack enable
and then just run

yarn
This will install the required version of yarn and resolve all dependencies.

Note

Corepack is a tool to help with managing versions of your package managers. It exposes binary proxies for each supported package manager that, when called, will identify whatever package manager is configured for the current project, download it if needed, and finally run it.

Initial setup
Clone the repository:
git clone <repo-url>
cd monorepo
Install dependencies:
yarn install
Monorepo commands
Here are some essential commands to help you navigate the monorepo:

Workspace management
Run a script in a specific workspace:
yarn workspace <workspace-name> <script>
Example:

yarn workspace @safe-global/web start
Add a dependency to a specific workspace:
yarn workspace <workspace-name> add <package-name>
Remove a dependency from a specific workspace:
yarn workspace <workspace-name> remove <package-name>
Note

Yarn treats commands that contain a colon as global commands. For example if you have a command in a workspace that has a colon and there isn't another workspace that has the same command, you can run the command without specifying the workspace name. For example:

yarn cypress:open
is equivalent to:

yarn workspace @safe-global/web cypress:open
Linting and formatting
Run ESLint across all workspaces:
yarn lint
Testing
Run unit tests across all workspaces:
yarn test
Contributing
Adding a new workspace
Create a new directory under apps/ or packages/.
Add a package.json file with the appropriate configuration.
Run:
yarn install
Best practices
Use Yarn Workspaces commands for managing dependencies.
Ensure tests and linting pass before pushing changes.
Follow the commit message guidelines.
Tools & configurations
Husky: Pre-commit hooks for linting and tests.
ESLint & Prettier: Enforce coding standards and formatting.
Jest: Unit testing framework.
Expo: Mobile app framework for the mobile workspace.
Next.js: React framework for the web workspace.
Useful links
Yarn Workspaces Documentation
Expo Documentation
Next.js Documentation
Jest Documentation
ESLint Documentation
Prettier Documentation
If you have any questions or run into issues, feel free to open a discussion or contact the maintainers. Happy coding! 🚀
