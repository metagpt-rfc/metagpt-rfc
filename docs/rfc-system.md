---
title: "RFC文档系统实现方案"
toc: true
date: 2023-10-27 15:00:00
tags:
- MetaGPT
- 系统设计
categories: 
- [系统设计]
---


文档修改历史
| 日期 | 版本 | 作者 | 修改内容 |
| --- | --- | --- | --- |
| 2023/10/05 | v0.1 |  |  |


本文档评审记录
| 审核人 | 邀请日期 | 审核日期 | 审核意见 |
| --- | --- | --- | --- |
|  |  |  |  |

# 背景
MetaGPT项目需要一个文档系统，能够让开发者参与RFC文档的编写和Review，Review通过的文档，发布到对外开放的平台。

# 目标
## 定义
1. 多用户协作的文档系统
2. 支持编写文档、评论、上传图片和文件
3. 支持多语言

<!--more-->

# 提案
## 思路
整个实现围绕着github：
1. 一个github仓库作为rfc文档存放仓库
2. 用户提交pr，markdown格式的rfc
3. 其他人在pr上review，评论
4. pr review修改完成后合入主分支，触发cicd
5. 主分支的rfc文档，自动部署到githubpage，hexo页面展示（或者在cicd时调用notion接口部署到notion）
6. hexo页面上，添加gitalk评论插件，用户评论会存到github issue

## 示例
https://metagpt-rfc.github.io/

# 开放讨论

# 附录
## 术语
| 术语 | 全称 | 解释 |
| --- | --- | --- |
| notion | notion |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

# 参考


