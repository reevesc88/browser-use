# Copilot Instructions — browser-use

Async Python library implementing AI browser driver abilities using LLMs + Playwright.

## Stack
- Python 3.11+ (async, type hints required)
- Playwright for browser automation
- Pydantic v2 for data models
- `uv` for package management

## Code Style
- Tabs for indentation (not spaces)
- Modern Python typing: `str | None` not `Optional[str]`, `list[str]` not `List[str]`
- Pydantic models: `model_config = ConfigDict(extra='forbid', validate_by_name=True)`
- Use `Annotated[..., AfterValidator(...)]` for validation logic
- Logging methods prefixed with `_log_`
- Service code in `service.py`, models in `views.py`

## Tests
- Run: `uv run pytest -vxs tests/ci`
- Never use real URLs (google.com etc.) — use pytest-httpserver
- No mocks except for LLM
- Passing tests go in `tests/ci/`

## Token Budget
See conductor-brain repo (CONTEXT_CONTROL.md) for agent delegation rules.
