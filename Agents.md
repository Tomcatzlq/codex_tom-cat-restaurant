# Agents.md

## 项目背景

这是一个名为“汤姆猫餐厅”的前端展示项目，目标是为一家现代融合风格餐厅提供品牌展示页、菜品介绍、空间氛围展示、季节菜单和预约引导。

当前项目已经从原始的单页 HTML 演进为 **Vite + Vue 3** 架构，更便于后续扩展组件、维护页面结构、新增交互功能，以及接入真实业务接口。

## 当前状态

- 项目类型：Vite + Vue 3
- 项目名称：Tom Cat Restaurant / 汤姆猫餐厅
- 当前运行地址：http://localhost:5173/
- 当前内容语言：中文为主
- 当前素材来源：Unsplash 占位图
- 当前性质：品牌展示前端原型，不是最终生产系统

## 项目目标

1. 作为餐厅的品牌展示站点原型
2. 展示餐厅定位、招牌菜、空间氛围、主厨理念和预约信息
3. 为后续功能扩展提供可维护的前端基础
4. 便于后续接入真实图片、真实菜单数据和真实预约流程

## 当前已完成内容

- 已将项目迁移到 Vue 工程结构
- 已拆分为多个组件，包括：
  - `NavBar`
  - `HeroSection`
  - `AboutSection`
  - `DishesSection`
  - `AmbianceSection`
  - `MenuSection`
  - `ChefSection`
  - `ReservationSection`
  - `SiteFooter`
- 已统一文案为中文，并将品牌名称统一为“汤姆猫餐厅”
- 已建立基础全局样式体系，保持暗色餐饮风格
- 已保留响应式布局适配思路

## 当前仍未完成的部分

- 尚未接入真实餐厅数据源
- 尚未接入真实图片资产
- 尚未实现预约表单提交逻辑
- 尚未添加路由系统
- 尚未添加多语言支持
- 尚未补充自动化测试
- 尚未做 SEO、性能、可访问性的系统优化

## 后续扩展方向

### 短期方向
- 把静态菜单数据抽离为 JSON 或 Composable
- 将页面中的硬编码图片替换为真实资产
- 增加移动端导航组件
- 增加轻量交互，例如菜单筛选、菜品详情弹窗、图片预览等

### 中期方向
- 引入 Vue Router，支持首页、菜单页、关于页、预约页等多页面结构
- 增加后台数据接口，支持动态菜单、活动信息、营业时间等配置化
- 增加预约系统基本表单、校验和提交流程
- 增加管理后台或 CMS 集成

### 长期方向
- 支持会员体系、优惠活动、营销落地页
- 支持多门店、多语言、多主题
- 支持 SEO SSR / SSG 方案
- 支持真实上线部署与监控体系

## 当前目录结构

- `index.html`
- `package.json`
- `vite.config.js`
- `README.md`
- `src/main.js`
- `src/App.vue`
- `src/styles.css`
- `src/components/NavBar.vue`
- `src/components/HeroSection.vue`
- `src/components/AboutSection.vue`
- `src/components/DishesSection.vue`
- `src/components/AmbianceSection.vue`
- `src/components/MenuSection.vue`
- `src/components/ChefSection.vue`
- `src/components/ReservationSection.vue`
- `src/components/SiteFooter.vue`

## 开发约定

- 页面以中文内容为主
- 品牌统一使用“汤姆猫餐厅”
- 组件尽量保持单一职责，不做过度抽象
- 样式优先保持现有视觉体系，不做无意义重构
- 后续新增功能时，优先保持体验一致性，再考虑技术扩展

## 当前风险与注意事项

- 当前页面使用外部图片链接，依赖网络环境
- 当前页面仍为展示型前端，不具备真实业务闭环
- 如果后续要上线，需要替换为真实素材、真实文案和真实接口
- 如果扩展成多页面应用，需要尽早引入路由和状态管理方案
