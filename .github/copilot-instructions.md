# Copilot Instructions for YT-MLOPS-CI-Masterclass

## Project Overview
This project demonstrates end-to-end Continuous Integration (CI) using a simple Streamlit app and associated tests. The main goal is to provide a clear, reproducible example of CI workflows for educational purposes.

## Architecture & Key Files
- `app.py`: Streamlit UI for calculating the square, cube, and fifth power of a user-provided integer. All logic is implemented inline for simplicity.
- `_test.py`: Contains pytest-based unit tests for the core mathematical functions (square, cube, fifth power). Also tests error handling for invalid input.
- `README.md`: Brief project description. No custom build/test instructions are provided here.

## Developer Workflows
- **Run the app locally:**
  ```powershell
  streamlit run app.py
  ```
- **Run tests locally:**
  ```powershell
  pytest _test.py
  ```
- **CI/CD:**
  No workflow files are present in this repo, but the project is designed for easy integration with GitHub Actions or similar CI tools. Typical workflows would:
    - Install dependencies (`streamlit`, `pytest`)
    - Run tests with `pytest`
    - Optionally deploy the Streamlit app

## Project Conventions
- All business logic is duplicated in both `app.py` (inline) and `_test.py` (as standalone functions for testability).
- Test file is named `_test.py` (not the default `test_*.py` pattern). Adjust CI/test discovery if needed.
- No requirements.txt or environment file is present; dependencies must be inferred from imports.
- No custom error handling or logging is implemented beyond basic assertions in tests.

## Integration Points
- **External dependencies:**
  - `streamlit` for the UI
  - `pytest` for testing
- No database, API, or external service integration.

## Examples
- To add a new mathematical operation, update both the UI logic in `app.py` and add corresponding test functions in `_test.py`.
- To change test discovery, rename `_test.py` to `test_app.py` or adjust your CI configuration.

---

For questions about project structure or workflows, refer to this file and the `README.md`. If you add new conventions, update this file to keep AI agents productive.
