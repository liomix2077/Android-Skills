
<h1 align="center">Android-Skills</h1>
<p align="center">
  <a href="README-EN.md">English</a>
</p>

<p align="center">
  <a href="https://developer.android.com"><img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Android"></a>
  <a href="https://kotlinlang.org"><img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white" alt="Kotlin"></a>
  <a href="https://developer.android.com/jetpack/compose"><img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-2C6BED?style=flat-square&logo=apache&logoColor=white" alt="License"></a>
</p>

## 简介

**Android-Skills** 是一个专为 Android 开发者整理的 Skills 整合包，汇集了以下三个优质来源：

| 来源 | 定位 | 使用策略 |
|------|------|----------|
| [android/skills](https://github.com/android/skills) | Google 官方 Android Skills库 | **优先使用**，覆盖平台标准、迁移指南、合规检查、CLI 工具等 |
| [chrisbanes/skills](https://github.com/chrisbanes/skills) | Chris Banes 的 Kotlin / Compose 深度实践 | **作为补充**，仅收录官方未覆盖或侧重不同的编码实践、架构与性能Skills |
| [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | 通用 UI/UX 设计Skills库 | **精简保留**，仅保留对 Android 开发有用的设计系统、品牌与 UI/UX Skills |

整合包遵循以下原则：

1. **官方优先**：同一Skills若官方已有，优先使用 `android/skills` 版本。
2. **补充为辅**：`chrisbanes/skills` 仅提供官方缺失的 Kotlin / Compose 编码内功。
3. **按需精简**：`ui-ux-pro-max-skill` 剔除 Web / Tailwind / shadcn 等无关内容。




## Skills清单

### 官方Skills（android/skills）

以下Skills全部来自 `android/skills`，是 Android 开发的首选参考：

| Skills | 用途 |
|------|------|
| `adaptive` | 适配手机、平板、折叠屏、桌面、TV、Auto、XR |
| `edge-to-edge` | 边到边显示、Insets 处理、IME 适配 |
| `jetpack-compose-performance` | Compose 性能诊断与优化 |
| `navigation-3` | Jetpack Navigation 3 迁移与使用 |
| `navigation-event` | 预测性返回手势与返回拦截 |
| `migrate-xml-views-to-jetpack-compose` | XML View 迁移至 Compose |
| `testing-setup` | 单元测试、UI 测试、截图测试基础设施 |
| `agp-9-upgrade` | 升级至 Android Gradle Plugin 9 |
| `android-cli` | 使用 `android` 命令行工具 |
| `camerax` | CameraX 相机开发 |
| `restore-credentials` | 免密登录与换机静默登录 |
| `verified-email` | 无 OTP 邮箱验证 |
| `appfunctions` | 向 Android 系统暴露 App 功能供 AI Agent 调用 |
| `android-permissions-security` | 权限与 IPC 组件安全审计 |
| `android-intent-security` | Intent 安全与重定向防护 |
| `play-policy-insights` | Google Play 政策合规检查 |
| `r8-analyzer` | R8 / ProGuard Keep 规则优化 |
| `play-billing-library-version-upgrade` | Google Play Billing Library 升级 |
| `android-profiler` | 系统 Trace、ANR、内存泄漏、耗电分析 |
| `leanback-to-compose-tv-migration` | Leanback 迁移至 Compose for TV |
| `android-for-cars-parked-apps` | 车机 parked app 适配 |
| `glance-canonical-layouts` | Jetpack Glance 桌面小部件 |

> 完整列表以 `android/skills` 官方仓库为准。

### 补充Skills（chrisbanes/skills）

以下Skills在官方仓库中不存在或侧重不同，作为补充收录：

| Skills | 用途 |
|------|------|
| `using-chrisbanes-skills` | Chris Banes Skills包的路由入口 |
| `compose-state-and-effects` | Compose 状态管理与副作用 |
| `compose-component-design` | 可复用 Compose 组件 API 设计 |
| `compose-animations` | Compose 动画与过渡 |
| `compose-performance` | 重组开销、编译器稳定性、可跳过性分析 |
| `compose-ui-testing-patterns` | Compose UI 测试与截图测试模式 |
| `kotlin-api-design` | Kotlin 函数、类、扩展、值类设计 |
| `kotlin-concurrency-and-flow` | 协程作用域、Flow、StateFlow 建模 |
| `kotlin-control-flow` | Kotlin 控制流、密封类型、智能转换 |
| `gradle-run` | Gradle 构建诊断与执行 |
| `grounded-writing` | 技术文档、博客、评审意见撰写 |
| `compose-focus-navigation` | TV、键盘、D-pad 焦点导航 |

### UI/UX 设计Skills（精简自 ui-ux-pro-max-skill）

仅保留对 Android 开发有帮助的Skills：

| Skills | 用途 |
|------|------|
| `ui-ux-pro-max` | UI/UX 设计智能，覆盖组件、布局、配色、字体、可访问性 |
| `design-system` | 设计 Token、组件规范、间距与字体比例 |
| `brand` | 品牌语调、视觉识别、品牌一致性 |
| `banner-design` | Google Play 宣传图、社交媒体素材（可选） |

> 已剔除：`ui-styling`（Web / shadcn / Tailwind）、`slides`（演示文稿）等与 Android 原生开发无关的Skills。



## 安装

### 方式一：使用 `npx skills` 批量安装

```bash
# 安装官方Skills（优先）
npx skills add https://github.com/android/skills \
  --skill adaptive \
  --skill edge-to-edge \
  --skill jetpack-compose-performance \
  --skill navigation-3 \
  --skill navigation-event \
  --skill migrate-xml-views-to-jetpack-compose \
  --skill testing-setup \
  --skill agp-9-upgrade \
  --skill android-cli \
  --skill camerax \
  --skill restore-credentials \
  --skill verified-email \
  --skill appfunctions \
  --skill android-permissions-security \
  --skill android-intent-security \
  --skill play-policy-insights \
  --skill r8-analyzer \
  --skill play-billing-library-version-upgrade \
  --skill android-profiler \
  --skill leanback-to-compose-tv-migration \
  --skill android-for-cars-parked-apps \
  --skill glance-canonical-layouts

# 安装 Chris Banes 补充Skills
npx skills add chrisbanes/skills  \
  --skill using-chrisbanes-skills \
  --skill compose-state-and-effects \
  --skill compose-component-design \
  --skill compose-animations \
  --skill compose-performance \
  --skill compose-ui-testing-patterns \
  --skill kotlin-api-design \
  --skill kotlin-concurrency-and-flow \
  --skill kotlin-control-flow \
  --skill gradle-run \
  --skill grounded-writing \
  --skill compose-focus-navigation

# 安装精简后的 UI/UX Skills
npx skills add nextlevelbuilder/ui-ux-pro-max-skill --global --yes \
  --skill ui-ux-pro-max \
  --skill design-system \
  --skill brand \
  --skill banner-design
```

### 方式二：手动复制

将各Skills文件夹复制到对应 Agent 的 skills 目录，例如：

- Claude Code：`~/.claude/skills/`
- Cursor：`~/.cursor/skills/`
- 其他 Agent：参考其官方文档





## 致谢

- [android/skills](https://github.com/android/skills) — Google 官方 Android Skills库
- [chrisbanes/skills](https://github.com/chrisbanes/skills) — Chris Banes 的 Kotlin / Compose 实践
- [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) — UI/UX 设计Skills库
