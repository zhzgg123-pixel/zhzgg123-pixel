# 项目展示

## OJ 自动化测试平台

面向在线判题系统的自动化测试工具，将用例生成、提交执行、结果断言和报告归档串成可复现的回归流程。

**技术栈：** Python · FastAPI · SQLite · pytest · Docker · GitHub Actions

### 核心能力

- **用例生成：** 使用 YAML 定义题目规则与程序模板，支持随机模板抽样、边界/异常模板和接口规则检查，并通过 seed 复现输入。
- **任务执行：** Web 与 CLI 共用任务服务，支持顺序执行、线程池并发、任务取消和历史查询。
- **结果验证：** 对比预期与实际判题结果，覆盖 AC、WA、CE、TLE、RE 等状态，并记录逐例差异。
- **报告与追溯：** 导出 HTML / JSON 报告，保存源码输入、题目配置和版本信息，便于定位失败与复现问题。
- **持续回归：** 使用 HTTP Mock 验证平台链路与故障场景，并通过固定版本的真实 C++ OJ 联调；GitHub Actions 运行回归并归档报告。

项目源码：[oj-test-platform](https://github.com/zhzgg123-pixel/oj-test-platform)。
