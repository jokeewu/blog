---
title: Jenkins+Github持续集成
categories: 
- CI
tags:
- 前端自动化
- 前端构建
- 前端部署
---

源于对现在部署方案的不满。

### 环境准备

- Github账号及测试项目
- 网络服务器一台，用于Github通过Webhooks调用通知
- 网络服务器需安装[Node](https://nodejs.org/),[Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git),[Jenkins](https://jenkins.io/doc/pipeline/tour/getting-started/)

<!--more-->

### 配置Github项目Webhooks

Step1: Github进入项目 > Settings

{% asset_img github-step1.jpeg %}

Step2: 选择Webhooks

{% asset_img github-step2.jpeg %}

其中Secret来源于Jenkins系统，用户 > [具体用户] > 设置 > API Token

{% asset_img jenkins-api-token.jpeg %}

### 配置Jenkins

Step1: 安装Generic Webhook Trigger插件

系统管理 > 管理插件 > 可选插件 > [输入Generic Webhook Trigger]安装

Step2: 新建任务

新建任务

{% asset_img create-task.jpeg %}

任务配置

Step1: 基础信息/项目类型

{% asset_img task-config-step1.jpg %}

Step2: 源码管理工具

{% asset_img task-config-step2.jpg %}

Step3: 触发器配置

{% asset_img task-config-step3.jpg %}

Step4: 构建过程脚本命令配置

{% asset_img task-config-step4.jpg %}

Step5: 构建邮件通知

{% asset_img task-config-step5.jpg %}

Step6: 测试成功

{% asset_img result-success.jpg %}


