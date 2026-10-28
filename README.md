# House Price Project: Git + DVC Data Versioning

Source code is versioned with Git, and the dataset is versioned with DVC.

## Versions

| Version | Rows | MD5 hash | Git tag |
|---|---|---|---|
| v1 (original) | 1460 | PASTE_V1_HASH | v1 |
| v2 (modified: dropped rows with missing LotFrontage) | 1201 | PASTE_V2_HASH | v2 |
| Restored v1 | 1460 | PASTE_V1_HASH (identical to v1) | v1 |

## Git history
```
PASTE git log --oneline --decorate OUTPUT
```

## v1 metadata (train.csv.dvc)
```
PASTE git show v1 OUTPUT
```

## v2 metadata (train.csv.dvc)
```
PASTE git show v2 OUTPUT
```

## How to recover the earlier version
```
git checkout v1 -- data/raw/train.csv.dvc
dvc checkout
```

## Verification after restore
- Shape returned to (1460, 81)
- MD5 hash identical to v1
- `dvc status`: PASTE OUTPUT