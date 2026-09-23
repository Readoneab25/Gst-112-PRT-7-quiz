# Sanctum Quiz — Reusable Template

This repository is a reusable quiz template connected to SanctumVault's central quiz-results system.

## Files

- `index.html` — quiz interface and engine.
- `quiz-config.js` — quiz identity, tutor branding, timer and settings.
- `quiz-questions.js` — question bank.

## Creating another quiz

1. Copy this repository/template for the new quiz.
2. In `quiz-config.js`, change:
   - `id` to a new unique ID.
   - `title`
   - `subject`
   - `quizNumber`
   - `tutorName`
   - `timeMinutes`
   - branding/logo when supplied.
3. Replace the questions in `quiz-questions.js`.
4. Keep the same Supabase result submission code in `index.html`.
5. Add the finished quiz URL in SanctumVault Admin → Tutor Quiz.

## Important

Do not reuse the same `id` for two different quizzes. Each quiz should have its own unique ID so all attempts can be identified correctly in SanctumVault.

Students do not need a SanctumVault account to take a quiz.

Every attempt is stored separately in the central `quiz_results` table. Authorized SanctumVault users can view the attempts from the private Quiz Results dashboard.

The Supabase publishable key used by the quiz is safe for browser use under the project's RLS/RPC security rules. Never put a Supabase service-role key in this repository.
