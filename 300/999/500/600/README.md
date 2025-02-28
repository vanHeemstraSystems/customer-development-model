# 600 - Continuous Integration

**Use Case**: Music

* **Information gathered**: You push your changes, triggering GitHub Actions to run:
  - Unit tests for the new audio control methods.
  - Integration tests for settings persistence.
  - UI component tests.

A failing test reveals that volume settings aren't persisting when changing audio sources. You fix the issue and commit again.

* **Tools**:

  - [GitHub](https://github.com/) (workflows): You push your changes, triggering GitHub Actions to run.
  - [ActivePieces](https://www.activepieces.com/) (automation): ...
  - [NotePlan](https://app.noteplan.co/) (documentation): ...