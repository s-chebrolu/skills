---
name: code-review
description: Perform thorough, actionable code reviews across any language or framework. Use this skill when the user asks to review, audit, critique, or improve existing code, including pull request reviews, security audits, performance analysis, or readability feedback.
---

This skill guides delivery of clear, actionable code reviews. Provide real analysis with specific suggestions and honest prioritization, not some generic comments.
 
The user provides code to review. They may include context about the language, framework, or what kind of feedback they want (security, performance, readability, etc.).
 
## Review Thinking
 
Before commenting, understand the code's context:
 
- **Purpose**: What is this code trying to do?
- **Scope**: Is this a small helper, a critical function, or a large module? Scale feedback accordingly.
- **Priority**: Make sure correctness first, then security, performance, and style.
**CRITICAL**: Prioritize findings clearly. Explain why each issue matters, not just that it exists. Every issue raised should include a concrete suggestion or corrected snippet.
 
## Code Review Guidelines
 
Cover these areas in every review:
 
- **Correctness**: Look for logic bugs, unhandled edge cases, and wrong assumptions about input.
- **Security**: Flag vulnerabilities like missing input validation or hardcoded secrets.
- **Performance**: Call out inefficiencies that would matter at real scale and skip any unnecessary micro optimizations.
- **Readability**: Note unclear naming, overly complex logic, or anything that would confuse a new contributor.
NEVER leave vague feedback like "this could be cleaner" without showing what cleaner looks like.
 
**IMPORTANT**: Match feedback depth to code size. A 20 line function needs less analysis than a 300 line class, but both deserve precise, useful comments.
