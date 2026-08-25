# 🛠️ Essential Git & Docker Recipes

A quick reference guide for common developer workflows in production environments.

---

## 🐙 Git Workflows

### Clean Squash Workflow
```bash
# Rebase and squash last N commits
git rebase -i HEAD~3

# Amend previous commit without editing commit message
git commit --amend --no-edit
```

### Undo Last Commit Keeping Changes
```bash
git reset --soft HEAD~1
```

---

## 🐳 Docker Snippets

### Prune Unused Images & Volumes
```bash
docker system prune -af --volumes
```

### View Real-time Container Stats
```bash
docker stats --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}\t{{.NetIO}}"
```
