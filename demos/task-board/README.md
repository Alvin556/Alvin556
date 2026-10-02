# Shared Task Board

Live board: https://claude.ai/artifact/7fMdZgCMrpq2f7Q64SJMLv

A single-page kanban board published as a Claude artifact with shared cloud
storage. Everyone with Contributor access sees the same tasks and changes
appear live.

## Features

- Columns: rename, reorder, add, remove (Columns button).
- Tasks: title, column, priority, assignee, client/project, due date, notes.
- Drag and drop between columns; arrow buttons on phones.
- Views: Board, By person, List. Search plus person and client filters.
- Read-only visitors get a banner instead of silent failures.

## Data model (artifact database)

- `board/config` : `{ name, columns: [{ id, name }] }`
- `tasks/<id>` : `{ title, column, priority (high|med|low), assignee, client, due (YYYY-MM-DD), notes, order, createdAt, updatedAt }`

## Republishing

Publish `task-board.html` to the same artifact URL. The database is kept
across republishes, so tasks and column settings are not lost.

## Sharing

Open the board, click Share, invite each person by email as Contributor.
