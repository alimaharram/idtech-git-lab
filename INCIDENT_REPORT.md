# Incident Report: Production API Endpoint Correction

## Problem
`feature/security` branch-ində təhlükəsizlik qeydləri yazılarkən IDTECH portalında prod API ünvanının yanlış olduğu aşkar edildi. Dərhal hotfix tələb olundu.

## İstifadə edilən Git əməliyyatları
1. **`git stash push`**: `feature/security` branch-indəki yarımçıq qeydlər iş mühitini təmizləmək üçün stash-ə saxlanıldı.
2. **`git checkout -b hotfix/api-endpoint`**: `main` branch-indən təcili hotfix branch-i ayrıldı.
3. **`git commit --amend`**: `config/app.env.example` və `README.md` fayllarındakı düzəlişlər birləşdirilərək hotfix tarixçəsində cəmi 1 commit saxlanıldı.
4. **`git merge`**: Hotfix `main` branch-inə birləşdirildi.
5. **`git stash pop`**: `feature/security` branch-inə qayıdaraq yarımçıq saxlanılmış işlər bərpa edildi və təhlükəsizlik qeydləri tamamlandı.

## Nəticə
Production API ünvanı (`https://api.idtech.example`) uğurla yeniləndi və `main` branch-inə merge edildi. Yarımçıq işlər təmiz şəkildə bərpa olunaraq tamamlandı, stash tam təmizləndi.
