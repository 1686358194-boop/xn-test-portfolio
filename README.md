# 🛡️ xn-test｜企业级Web安全评估报告

## 📌 1. 项目概述
本项目基于 DVWA 靶场，对常见Web安全漏洞进行复现、分析与风险评估，模拟企业安全测试流程。

覆盖漏洞：
- SQL Injection
- XSS（Stored / Reflected）
- HTTP请求篡改（Burp Suite）

---

## 🎯 2. 安全评估目标
- 识别Web应用攻击面
- 验证输入输出安全问题
- 分析漏洞影响范围
- 提供企业级修复建议

---

## 🧱 3. 测试架构
Browser → Burp Suite → DVWA → Database

---

## ⚠️ 4. 风险汇总

| 漏洞 | 等级 | 影响 |
|------|------|------|
| SQL Injection | 高危 | 数据泄露 / 认证绕过 |
| Stored XSS | 高危 | 会话劫持 |
| Reflected XSS | 中高危 | 钓鱼攻击 |

---

## 🧪 5. 漏洞分析

### SQL Injection
- 输入未过滤直接拼接SQL
- 可构造 OR 1=1 绕过查询

**修复：**
- Prepared Statement
- 参数化查询

---

### XSS
- 未做输出编码导致脚本执行

**修复：**
- HTML转义
- CSP策略
- HttpOnly Cookie

---

### Burp分析
- 拦截HTTP请求
- 修改参数验证漏洞
- 重放请求验证行为

---

## 📊 6. 风险评级模型
- Critical：系统级控制
- High：数据泄露
- Medium：信息泄露
- Low：轻微暴露

---

## 🧠 7. 安全能力总结
- Web漏洞原理分析
- HTTP协议理解
- 基础渗透测试流程
- Burp Suite使用
- 安全修复思维

---

## 🚀 8. 面试一句话总结
本项目用于验证Web常见漏洞原理与攻击路径，并提供完整风险分析与修复方案。

