Investigate the following bug in this existing legacy codebase.

BUG DESCRIPTION
[Describe the bug here if it is short. Otherwise, save your bug details into one or more files and upload the file(s). Review all attached files as part of the bug investigation.]

GOAL
Identify the root cause, analyze the impact scope, and recommend the smallest safe fix. Do not implement the fix.

INVESTIGATION

1. Understand the Existing Code
- Locate the relevant source code, entry points, functions, services, APIs, and database operations.
- Trace the actual execution path and data flow.
- Understand existing business rules and dependencies.
- Do not assume documentation accurately reflects current behavior.

2. Reproduce the Bug
- Review the bug description and all attached files before investigating.
- Reproduce the issue when practical.
- Examine logs, error messages, existing tests, configurations, and recent code changes when available.
- Record reproduction steps and observed behavior.
- If reproduction is not possible, explain why and continue with static code analysis.

3. Root Cause Analysis
- Identify the underlying cause rather than only the visible symptom.
- Trace the relevant execution path to the defective logic.
- Provide evidence using source file paths, functions, and line numbers.
- Distinguish confirmed findings from hypotheses.
- Explicitly state when the root cause cannot be verified.

4. Impact Scope / Blast Radius
- Identify affected modules, functions, APIs, workflows, and integrations.
- Examine upstream callers and downstream dependencies.
- Check shared libraries, business rules, database queries, stored procedures, and triggers.
- Determine whether other customers, tenants, or sales channels may be affected.
- Identify existing data that may already be incorrect.
- Separate confirmed impact from potential impact.
- Consider the potential side effects of the recommended fix.

5. Suggested Fix
- Recommend the smallest safe fix compatible with existing legacy behavior.
- Identify specific source files, functions, and logic requiring modification.
- Explain why the proposed fix addresses the root cause.
- Compare alternative solutions when relevant.
- Avoid unnecessary refactoring or architectural redesign.
- Do not implement the fix.

6. Regression Tests and Verification
- Recommend tests to verify the bug is resolved.
- Include normal cases, edge cases, and previously working scenarios.
- Identify possible regressions in related modules and workflows.
- Include database and integration verification when applicable.
- Consider deployment risks, historical data repair, and rollback requirements.

7. Skills and Tools
- Use relevant installed skills, such as diagnosing-bugs, PStack how-and-why, and PStack blast-radius, when available.
- Verify skill availability rather than assuming a skill exists.
- Use repository search, Git history, tests, and code analysis tools as needed.
- Do not automatically invoke implementation workflows or modify source code.

DELIVERABLE A: DETAILED TECHNICAL HANDOFF

Save the report to:
investigations/<bug-id>/HANDOFF.md

Include:
- Bug description and expected versus actual behavior
- Relevant code architecture and execution flow
- Reproduction steps and evidence
- Root cause analysis
- Impact scope / blast radius
- Proposed fix with specific code references
- Regression test plan
- Deployment, data repair, and rollback considerations
- Unresolved questions and confidence level
- Repository commit and exact source file paths and line numbers where available

DELIVERABLE B: JIRA-READY REPORT

Save the report to:
investigations/<bug-id>/BUG-ANALYSIS-AND-FIX-SUGGESTION.md

Title:
Bug Analysis and Fix Suggestion

Use these exact sections:

1. Bug Summary
   - Briefly describe the bug.
   - Explain expected and actual behavior.

2. Root Cause Analysis
   - Explain the underlying technical cause.
   - Identify relevant source files, functions, and logic.
   - Include supporting evidence.
   - Clearly identify unverified hypotheses.

3. Impact Scope
   - Identify affected modules, APIs, workflows, integrations, and data.
   - Describe potential impact on other customers or tenants.
   - Separate confirmed impacts from possible impacts.

4. Suggested Fix
   - Describe the recommended solution.
   - Identify the specific code changes developers should make.
   - Explain why this is the safest approach for the legacy codebase.
   - Mention alternatives when relevant.

5. Regression Tests / Verification
   - List recommended test scenarios.
   - Include edge cases and related workflows.
   - Explain how to verify the fix.

6. Risks and Considerations
   - Identify compatibility risks, side effects, dependencies, and deployment considerations.
   - Mention historical data repair or rollback needs when applicable.

7. Investigation Status
   - State whether the root cause is confirmed, probable, or undetermined.
   - Summarize any verification limitations or outstanding questions.
   - Make clear that the proposed fix has not been implemented.

JIRA REPORT REQUIREMENTS
- Make the report concise, professional, and self-contained.
- Format it so the entire content can be copied directly into a Jira ticket description or comment.
- Use clear headings and bullet points.
- Include specific source file paths and function names where useful.
- Avoid unnecessary implementation details and investigation logs.
- Do not include unsupported claims.
- Do not claim tests passed unless they were actually executed successfully.
- Do not claim the bug is fixed.

FINAL RESPONSE

Display the COMPLETE Jira-ready "Bug Analysis and Fix Suggestion" report in the conversation so I can copy and paste it directly into Jira.

Also provide:
- The saved paths for both Markdown reports.
- A brief summary of major findings.
- Any unresolved uncertainties or missing evidence.

CONSTRAINTS
- This is a read-only investigation.
- Do not modify application source code.
- Do not change database schemas or production data.
- Do not implement the proposed fix.
- Do not automatically update Jira tickets.
- Do not create commits or pull requests.
- Ask questions only when essential information blocks meaningful investigation.
- If no bug ID is provided, use a descriptive local folder name.
- If attached files contain conflicting information, identify the conflicts and explain them.
- Never invent source references, evidence, or test results.
