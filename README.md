# SQLite Desk Studio (HTA)

Small Windows HTA tool for browsing and editing SQLite databases using the
bundled `sqlite3.exe`.

## Requirements

- Windows with HTA support
- `sqlite3.exe` in the same directory as `admin.hta`

## Run

Double-click `admin.hta`.

## Configuration (`admin.ini`)

Create/edit `admin.ini` next to `admin.hta`:

```
;password=123456
pagerows=10
basepath=
```

- `password` (optional): if set, a login prompt is shown.
- `pagerows` (optional): rows per page (default 25).
- `basepath` (optional): relative path from the app folder to the database
  directory. If empty or missing, the app folder is used.

Examples:

- `basepath=db` -> databases are in `<app>\db`
- `basepath=..\data` -> databases are in `<app>\..\data`
- `basepath=C:\data\sqlite` -> absolute path is used

## Notes

- The app scans the database directory for `*.sqlite` files.
- New/renamed/copied databases are created in the same database directory.

