# Codex Pets 新手选择与安装指南

这个仓库用来记录你从 [Codex Pets](https://codex-pets.net/#/?sort=popular&kind=person) 挑选、下载、保存并安装到 Codex 的宠物。

适合完全新手：从打开网站开始，到把喜欢的 pet 放进 Codex。

## 你会得到什么

- 一份一步一步的中文教程
- 一个存放下载宠物包的位置
- 一个记录自己喜欢的 pet 的清单模板
- 上传到 GitHub 后，可以把这个仓库当作自己的 Codex pet 收藏夹

## 第 1 步：打开 Codex Pets 网站

1. 打开浏览器。
2. 进入这个网址：

   ```text
   https://codex-pets.net/#/?sort=popular&kind=person
   ```

3. 这个页面会按 popular 排序，并筛选 person 类型的宠物。
4. 如果页面没有马上显示内容，刷新一次浏览器。

说明：`codex-pets.net` 一般不需要登录就能浏览和下载。你需要登录的是 GitHub 或 Codex 应用本身。

## 第 2 步：挑选你喜欢的 pet

1. 在页面中上下滚动，查看不同的 pet。
2. 找到喜欢的角色后，点击它的卡片或详情入口。
3. 在详情页里先看预览动作，例如：
   - Idle
   - Run Right
   - Run Left
   - Wave
   - Jump
   - Failed
   - Waiting
   - Run
   - Review
4. 如果你喜欢这个 pet 的样子和动作，就继续下载。

## 第 3 步：下载 pet

1. 在 pet 详情页点击 `Download` 或 `Free Download`。
2. 浏览器会下载一个 `.zip` 文件。
3. 下载完成后，不要直接删除这个 zip。建议先放到本仓库的 `downloads/` 文件夹里保存。

推荐命名方式：

```text
downloads/pet-name.zip
```

例如：

```text
downloads/dad-coder.zip
```

## 第 4 步：解压 pet

1. 双击下载好的 `.zip` 文件解压。
2. 解压后通常会看到这些文件：
   - `pet.json`
   - `spritesheet.webp` 或 `spritesheet.png`
   - `preview.webp` 或 `preview.png`
   - 可能还有 `validation.json`、`source-sheet.png`
3. 把解压后的完整文件夹放到本仓库的 `pets/` 目录中。

推荐结构：

```text
pets/
  dad-coder/
    pet.json
    spritesheet.webp
    preview.webp
```

## 第 5 步：安装到 Codex

在 macOS 或 Linux 上，Codex 自定义 pet 通常放在：

```text
~/.codex/pets/
```

如果你的 pet 文件夹叫 `dad-coder`，最终路径应该类似：

```text
~/.codex/pets/dad-coder/
  pet.json
  spritesheet.webp
```

复制方式：

```bash
mkdir -p ~/.codex/pets
cp -R pets/dad-coder ~/.codex/pets/
```

然后打开 Codex：

1. 打开 Codex App。
2. 进入 `Settings`。
3. 找到 `Appearance`。
4. 打开 `Pets`。
5. 选择你刚刚安装的自定义 pet。
6. 在 Codex 输入框里输入：

   ```text
   /pet
   ```

7. 你的 pet 就会出现。再次输入 `/pet` 可以收起。

## 第 6 步：记录你的收藏

把你喜欢的 pet 记录到 [pets-list.md](./pets-list.md)。

建议记录：

- pet 名字
- 下载网址
- 是否已经安装
- 你喜欢它的原因

## 第 7 步：上传到你的 GitHub

如果你还没有登录 GitHub CLI，先运行：

```bash
gh auth login
```

按提示选择：

1. `GitHub.com`
2. `HTTPS`
3. `Login with a web browser`
4. 复制终端里的验证码
5. 在浏览器中登录 GitHub 并确认授权

登录后，在这个文件夹里运行：

```bash
git init
git add .
git commit -m "Add Codex Pets beginner guide"
gh repo create codex-pets-guide --public --source=. --remote=origin --push
```

如果你想建私有仓库，把 `--public` 换成：

```bash
--private
```

## 常见问题

### 我需要登录 codex-pets.net 吗？

通常不需要。你可以直接打开网站浏览、预览和下载。

### 下载后 Codex 找不到 pet 怎么办？

检查这三件事：

1. 文件夹是否放在 `~/.codex/pets/` 下面。
2. 文件夹里是否有 `pet.json`。
3. 文件夹里是否有 `spritesheet.webp` 或 `spritesheet.png`。

### pet 没有动怎么办？

先确认你在 Codex 里输入了：

```text
/pet
```

然后去 `Settings > Appearance > Pets` 检查是否选中了对应 pet。

## 参考链接

- [Codex Pets person popular 页面](https://codex-pets.net/#/?sort=popular&kind=person)
