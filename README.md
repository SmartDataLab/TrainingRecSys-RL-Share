---
marp: true
theme: gaia
_class: lead
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# 基于强化学习的员工学习内容的序列推荐技术研究

人大统院杨翰方课题组 苏锦华

---

## 需求场景

为什么员工需要不断学习：高技术行业最有价值的资产就是员工，员工拥有大量没有形成书面学习材料的知识经验，这是公司非常重要的资产，核心员工的流失意味着业务能力的流失。如果员工不具备竞争力的知识经验、公司就不具备竞争壁垒，对抗不可逆的员工流失的最好办法是形成知识沉淀系统和员工学习系统。

- 员工学习不足与公司学习材料过载(information overload)
- 集中培训培训费时,个性化培训更重要
- 1+1<2?团队综合能力大于个人平均能力

---

中石油业务线复杂，特定工种乏个性化的技能强化培训，同工种内不同人员的技能水平通常也有差异，学习材料的分发、学习路径的推荐以及学习成果的检验亟待个性化解决方案。

针对不同工种的学习培训材料、测试材料进行半监督标注、分级，给出表征学习方案。针对不同工种员工提供技能测试方案，根据测试结果、绩效考核、人事信息等多源信息提供学习材料推荐、学习路径自动规划，利用强化学习对员工的后续测试以及技能提升水平进行评估与进一步的学习路径选择。

---

## 好的实践

坚果云

简道云

问鼎云学习

SAP Litmos

[云学堂](https://lx.yxt.com/trainsaas/m?utm_term=%E5%91%98%E5%B7%A5%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F%E5%93%AA%E4%B8%AA%E5%A5%BD%E7%94%A8%E5%B8%8C%E6%9C%9B%E7%BB%99%E5%87%BA%E8%AF%A6%E7%BB%86%E4%BB%8B%E7%BB%8D&utm_campaign=268006449&utm_medium=zhihu&utm_source=zhihu_ziran&utm_content=%E6%83%B9%E6%83%B9%E5%9B%9E%E7%AD%94-%E4%BA%91%E5%AD%A6%E5%A0%82%E5%9C%A8%E7%BA%BF%E4%BC%81%E4%B8%9A%E5%9F%B9%E8%AE%AD%E5%B9%B3%E5%8F%B0-1)

考试云

[欢雀hr绩效管理系统](http://www.que360.com/activity/jixiaoguanli)

---

## 员工学习材料自动标注技术

带智能搜索和自助分类关系的文件系统(对多模态信息具有识别处理能力)，具有一定的加密和权限能力。

公告、内网技术博文、公司刊物、内部学习材料、培训材料、标准工作流、系统操作手册、咨询材料、课题报告、培训影像等具有公开分享属性的学习材料。

taxonomy strategy automation.

与组织架构脱钩、没有知识积累效应

信息过载所带来的影响：

解决模糊查找问题、适用于量化考核员工对岗位信息熟悉程度（指公司规范、操作手册）、为个性化学习材料的推荐提供item数据基础

针对非结构化的学习材料、测试材料进行分类分级(hierarchical toxonomy classification, AI for library sciences)，结合人工标注给出半监督、弱监督的分类方法，并对含图表的多模态长文本给出表征学习方案(representations for table aware&figure aware long text)。

---

## 利用用户标签的学习材料推荐系统

对于文件更新以及员工考核KPI或OKR相关的材料，比如说年度计划、年度总结、优秀员工经验分析能材料，应当具备分段、过滤、排序、交互式标注、推荐的能力，实现个性化材料推送。

融合绩效、测试结果等多源信息给出学习材料的推荐，并利用分类分级模型对学习材料进行学习路径规划(topological ordering recommendation, curriculum)，并给出针对学习路径的多段测评材料分发(Sequential Recommendation)。

filtering
ranking
topological ordering and sequence recommand

colaborative filtering and Recommand

---

## 结合团队绩效的个性化材料推荐

员工对学习材料的学习是一个过程，其间涉及多个测试和绩效反馈，同时技能互补的员工团队在解决问题上更具有合作优势，员工的技能培训也存在个体与团队效益的博弈。利用多用户强化学习（multi-agent reinforcement learning）对员工的技能提升程度进行自动评估与学习路径的动态调整，构建员工学习管理系统(Learning Management System, LMS)。
