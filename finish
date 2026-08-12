#!/usr/bin/env bash
# finish-release.sh — commit the release files and push the branch
set -euo pipefail
BRANCH="${1:-release/0.1.0}"

# sanity: never commit a real .env
if git ls-files | grep -qE '(^|/)\.env$'; then
  echo "❌ A .env file is committed. Remove it first."; exit 1
fi

git checkout -b "$BRANCH" 2>/dev/null || git checkout "$BRANCH"
git add -A
git commit -m "chore: release 0.1.0 — docs, license, CI, security policy

- README / CONTRIBUTING / SECURITY / CHANGELOG
- MIT license, editorconfig, prettier config
- GitHub Actions CI (typecheck + secrets scan) and Dependabot
- mobile .env.example"
git push -u origin "$BRANCH" 2>/dev/null \
  || echo "⚠️  Push manually:  git push -u origin $BRANCH"
