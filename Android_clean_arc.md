```
ProjectRoot/
├── gradle/                              # Gradle 配置目录
│   └── libs.versions.toml              # 依赖版本管理
│
├── app/                                # 主应用模块
│   ├── build.gradle.kts
│   └── src/main/
│       ├── java/com/example/app/
│       │   ├── di/                     # Hilt 应用级依赖注入
│       │   │   └── AppModule.kt
│       │   ├── navigation/             # 主导航配置
│       │   │   ├── NavGraph.kt
│       │   │   └── NavRoute.kt
│       │   ├── ui/
│       │   │   └── MainActivity.kt
│       │   └── App.kt
│       └── res/
│
├── core/                              # 核心模块目录
│   ├── core-ui/                      # UI 核心模块
│   │   ├── build.gradle.kts
│   │   └── src/main/kotlin/com/example/core/ui/
│   │       ├── theme/                # Compose 主题
│   │       │   ├── AppTheme.kt
│   │       │   ├── Color.kt
│   │       │   └── Type.kt
│   │       ├── components/           # 共享 Compose 组件
│   │       │   ├── AppBar.kt
│   │       │   ├── Buttons.kt
│   │       │   └── TextFields.kt
│   │       └── modifiers/           # 自定义 Compose modifiers
│   │
│   ├── core-data/                   # 数据层核心
│   │   ├── build.gradle.kts
│   │   └── src/main/kotlin/com/example/core/data/
│   │       ├── di/
│   │       ├── repository/
│   │       ├── remote/              # 网络相关
│   │       │   ├── api/
│   │       │   └── model/
│   │       └── local/               # 本地存储
│   │           ├── database/
│   │           └── datastore/
│   │
│   └── core-common/                # 通用工具
│       ├── build.gradle.kts
│       └── src/main/kotlin/com/example/core/common/
│           ├── extension/
│           ├── util/
│           └── result/            # 统一结果处理
│
├── features/                      # 功能模块目录
│   ├── feature-auth/             # 认证功能模块
│   │   ├── build.gradle.kts
│   │   └── src/main/kotlin/com/example/feature/auth/
│   │       ├── data/             # 数据层
│   │       │   ├── repository/
│   │       │   ├── remote/
│   │       │   └── mapper/
│   │       ├── domain/           # 领域层
│   │       │   ├── model/
│   │       │   ├── repository/
│   │       │   └── usecase/
│   │       └── presentation/     # 表现层
│   │           ├── login/        # 登录功能
│   │           │   ├── LoginScreen.kt
│   │           │   ├── LoginViewModel.kt
│   │           │   └── LoginUiState.kt
│   │           └── register/     # 注册功能
│   │
│   ├── feature-home/            # 首页功能模块
│   │   └── [与 feature-auth 相似结构]
│   │
│   └── feature-profile/         # 个人资料模块
│       └── [与 feature-auth 相似结构]
│
├── build.gradle.kts              # 项目级构建脚本
├── settings.gradle.kts           # 项目设置
└── gradle.properties            # Gradle 属性配置
```