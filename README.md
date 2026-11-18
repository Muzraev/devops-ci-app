# devops-ci-app

Учебное Flask-приложение для практической работы № 10.

CI: Pylint → pytest → Docker build → smoke-test → GHCR.
Публикация образа выполняется только из `main`.
В Pull Request выполняются проверки без публикации.

- health endpoint: `/health`;
- образ: `ghcr.io/muzraev/devops-ci-app`;
- основной workflow: `.github/workflows/ci.yml`.

После успешной проверки main публикуются два тега одного образа: полный SHA коммита и `latest`.
Для воспроизводимого развёртывания используется тег полного SHA.
