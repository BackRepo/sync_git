# Sync git repository

Use Github Action to synchronize git repository to gitlab.

## Description

This script will run automatically every day at 01:00.

## Configuration

SECRET|NOTES
---|---
GITLAB_USERNAME| Gitlab's username
GITLAB_USERMAIL| Gitlab's email
GITLAB_PASSWORD| Gitlab's password

## Mirrored git repository

View `REPO_URL` in `matrix` in `.github/workflows/sync.yml` file

## Gitlab's group

Go to https://gitlab.com/mirrors_git
