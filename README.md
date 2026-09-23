# 我的日程 — 个人课表与日程管理

零依赖、单文件、离线可用的个人日程管理应用。Neo-Brutalism 视觉风格。

## 功能

- **课表视图** — 按周展示课程安排，支持 1-11 节课时段，自动计算周次
- **日程管理** — 创建/编辑/删除待办事项，按日期分组，自动标记过期
- **首页概览** — 今日课程、下一节课倒计时、待办统计、无固定时间任务
- **备份恢复** — JSON 导出/导入，支持 localStorage 持久化
- **响应式布局** — 桌面端 Tab 导航 + 移动端底部 Tab Bar + FAB 快捷按钮
- **自测系统** — URL 添加 `?selftest=1` 运行 40 项自动化测试

## 技术

| 项目 | 选型 |
|------|------|
| 架构 | 单 `index.html`，零构建，零依赖 |
| 存储 | localStorage（`schedule-app-v1`） |
| 字体 | Space Grotesk（Google Fonts，离线回退系统字体） |
| 风格 | Neo-Brutalism：硬边零圆角、粗边框、硬偏移阴影、高饱和撞色 |
| 课表渲染 | CSS Grid + 绝对定位色块 |

## 使用

直接在浏览器中打开 `index.html` 即可。

```bash
# 或本地起一个服务
npx serve .
```

## 校历配置

默认使用北京航空航天大学 2026-2027 秋季学期校历：

- 开学日期：`2026-09-07`
- 总周数：`19`
- 修改方式：编辑 `CONST.SEMESTER_START` 和 `CONST.TOTAL_WEEKS`

## 自测

```
index.html?selftest=1
```

自动运行 40 项测试，覆盖日期计算、课表定位、日程 CRUD、备份恢复等核心逻辑。

## 仓库

<https://github.com/houchenfeng/schedule-manager>

## License

MIT
