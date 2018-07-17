### Test formatting on precommit hook with
 - precise-commits 1.0.2
 - prettier 1.13.7
 - husky 0.14.3
#### 1. Apply patch (whitespaces-only changes)
```sh
patch -p0 test01.ts < patch01.diff
```
#### 2. Check expecting prettier formating
```sh
node ../node_modules/prettier/bin-prettier.js test01.ts
```
#### 3. Commit
```sh
git add test01.ts
git commit -m "test01 format"
```
#### 4. Check results
```sh
cat test01.ts
```
