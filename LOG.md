---
title: "Wiki Log"
type: log
created: 2026-04-25
updated: 2026-05-22
description: 操作日志，按时间倒序排列，只追加不修改
---

# Wiki Log

> Chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete

## [2026-05-22] reset | 清理所有内容，恢复初始状态

- wiki/ 下所有 sources、entities、concepts、comparisons、reviews 页面已删除
- assets/images/ 下所有图片已删除
- INDEX.md、OVERVIEW.md 恢复为空白初始状态
- raw/ 保留不变

---

## [2026-05-22] ingest | 基于EnergyPlus的大型建筑负荷实时预测系统研究

- 来源：《建筑经济》2024年第45卷S2期，高秀洁/刘海隆
- 提取图表：fig_01~fig_05（5张含图注图片），table_01~table_05（5个Markdown表格）
- 创建来源页：[[sources/基于EnergyPlus的大型建筑负荷实时预测系统研究-2024]]
- 创建实体页：[[entities/高秀洁]]、[[entities/刘海隆]]、[[entities/EnergyPlus]]、[[entities/LSTM]]
- 创建概念页：[[concepts/EnergyPlus仿真]]、[[concepts/LSTM长短期记忆网络]]、[[concepts/建筑冷热负荷预测]]、[[concepts/建筑节能]]
- 更新 INDEX.md（10页面/4实体/4概念/1来源）、OVERVIEW.md
- 资产目录：assets/images/energyplus-lstm-building-load-prediction/

## [2026-05-22] ingest | 基于EnergyPlus的被动式建筑能耗仿真实验

- 来源：《实验技术与管理》2024年第41卷第7期，徐春雯等
- 提取图表：ref_p2~ref_p7（6张完整页面渲染，含11图+2表）
- 创建来源页：[[sources/基于EnergyPlus的被动式建筑能耗仿真实验-2024]]
- 创建实体页：[[entities/徐春雯]]、[[entities/罗昔联]]、[[entities/青岛宏海绿能]]
- 创建概念页：[[concepts/被动式建筑]]、[[concepts/灰色关联分析]]、[[concepts/虚实结合实验教学]]
- 更新已有页面：[[entities/EnergyPlus]]（+来源2）、[[concepts/建筑节能]]（+来源2）
- 更新 INDEX.md（20页面/7实体/7概念/2来源）、OVERVIEW.md
- 注：PDF图表由矢量碎片构成，改用完整页面渲染替代单独提取
- 脚本修复：extract_pdf_assets.py 添加 CMYK→RGB 颜色空间转换
- 资产目录：assets/images/passive-building-energyplus-simulation/

## [2026-05-22] ingest | 基于EnergyPlus的某高校供暖系统运行节能优化分析

- 来源：《建筑热能通风空调》2020年第39卷第11期，焦震/姜海洋
- 提取图表：fig_01~fig_15（15张带图注图片）
- 创建来源页：[[sources/基于EnergyPlus的某高校供暖系统运行节能优化分析-2020]]
- 创建概念页：[[concepts/供暖系统间歇运行]]
- 更新已有页面：INDEX.md（25页面/3来源/8概念）、LOG.md
- 脚本修复：extract_pdf_assets.py 修复 is_monochrome 属性错误，改用 n>=4 判断颜色空间
- 资产目录：assets/images/energyplus-university-hvac-optimization/

---

*日志仅追加，不修改历史记录*
