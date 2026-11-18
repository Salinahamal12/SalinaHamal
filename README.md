Set up this ABS Eagle QA automation project on my local Windows computer:

https://dev.azure.com/abs-eagle-engineering/Next-Gen-Eng-Apps/_git/ABS_NX_Gen_AUTO_TEST_WINUI

Goal: prepare a contributor workspace where I can use Copilot or an AI
agent to create and maintain automated tests from Azure PR/ticket links.

Please perform the setup, not just explain the steps:

1. Check that this computer is Windows and identify available tools.
   Ask where to clone the project if no suitable workspace is provided.
   If a checkout already exists, verify its remote and preserve all local
   changes. Do not overwrite it, reset it, or pull changes without approval.

2. Clone the repository. If Git or repository authentication is missing,
   guide me through the approved installation/sign-in process.
   Never request passwords, PATs, or license keys in chat.

3. Read AGENTS.md and its mandatory documents in the specified order.
   Then read .github/copilot-instructions.md and docs/SETUP.md.
   Follow the repository's setup, execution, and data-safety rules.

4. Run this read-only prerequisite check from the repository root:
   .\scripts\Setup-DevEnvironment.ps1 -CheckOnly

5. Summarize missing or unsupported dependencies and ask for approval
   before each installation. Use the existing setup script and approved
   installation sources rather than inventing another setup process.
   Include HTML report dependencies by default.

   The guided installation command is:
   .\scripts\Setup-DevEnvironment.ps1 -InstallMissing

   It requires interactive confirmations. If your terminal cannot handle
   them, guide me through running it locally. Do not auto-answer approvals,
   bypass corporate restrictions, or change machine-wide execution policy.

6. Once prerequisites are ready, use the setup script to restore packages,
   build Release, and run its focused offline tests:
   .\scripts\Setup-DevEnvironment.ps1

   If the guided installation run already completed this validation
   successfully, use its results instead of repeating the same work.
   Stop and report any failure. Do not claim readiness from a build alone.

7. Help me verify Azure access using the explicit organization:
   https://dev.azure.com/abs-eagle-engineering

   Guide interactive sign-in when needed. Verify access to this repository
   without exposing credentials. Do not assume this also grants access to
   application PRs, build artifacts, fixtures, or technical documentation.

8. Help me open the checkout in VS Code, sign in to Copilot, and select
   Agent mode. Ask me to confirm Workspace Trust and that the project
   instructions and seven skills are discovered. Do not claim entitlement
   or discovery is verified merely because their files exist.

9. Finish with a concise readiness summary:
   - Local checkout path and branch
   - Dependency versions and remaining actions
   - Build and offline-test results, including suite ID
   - Azure access verified or blocked
   - Copilot guidance discovered or awaiting my confirmation
   - Next steps for separately approved desktop testing

Boundaries:
- Do not install, uninstall, replace, or launch Eagle.
- Do not run desktop tests or an unfiltered test suite.
- Do not modify source or dependency manifests just to make setup pass.
- Do not commit, push, or post Azure comments/votes/work-item updates.
- Preserve existing projects, fixtures, credentials, and local changes.
- Separate offline readiness from application-test readiness.

After setup, give me a starter prompt for reviewing an Azure PR or ticket
without launching Eagle or posting anything.
