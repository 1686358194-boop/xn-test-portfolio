# xn-test｜Web安全渗透测试作品集

## 👤 一、项目定位
本项目基于 DVWA 靶场完成 Web 安全漏洞复现与验证，重点覆盖：
- SQL Injection（SQL注入）
- XSS（存储型 / 反射型）
- Burp Suite 流量分析与请求篡改

目标能力：
👉 Web漏洞原理理解 + 攻击验证 + 基础安全分析能力

---

## ⚙️ 二、技术栈
- DVWA（漏洞靶场）
- Burp Suite（抓包 / Repeater）
- Chrome DevTools
- HTTP协议分析
- 基础SQL语句与PHP执行逻辑

---

## 🧠 三、核心能力
✔ Web安全基础能力  
✔ OWASP Top 10理解  
✔ SQL注入攻击链分析  
✔ XSS攻击与数据窃取风险理解  
✔ Burp Suite抓包与重放  
✔ HTTP请求参数篡改能力  

---

## 📁 四、项目结构
```
xn-test/
├── README.md
├── DVWA-Lab/
│   ├── xss.md
│   ├── sql-injection.md
├── burp-notes.md
├── assets/screenshots/
```

---

## 💥 五、漏洞复现说明

### 1️⃣ SQL Injection

#### 攻击点
```text
?id=1' OR 1=1 --
```

#### 现象
- 绕过查询逻辑
- 返回管理员数据
- 数据库报错信息泄露

#### 安全本质
SQL拼接未做参数化处理

#### 🔒 修复方式
- 使用 Prepared Statement
- 输入过滤
- 最小权限数据库账号

---

### 2️⃣ XSS（Stored / Reflected）

#### Payload
```html
<script>alert(document.cookie)</script>
```

#### Stored XSS特点
- 数据被存储
- 所有访问者都会触发

#### Reflected XSS特点
- URL即时触发
- 无存储过程

#### 🔒 防御
- HTML转义
- CSP策略
- HttpOnly Cookie

---

### 3️⃣ Burp Suite分析

#### 流程
```
浏览器 → Proxy → Burp → 修改请求 → Repeater验证
```

#### 能力点
- HTTP请求结构分析
- 参数修改验证漏洞
- 重放攻击模拟

---

## 📷 六、截图证据
见 assets/screenshots（真实DVWA环境验证）

---

## 🧠 七、项目理解与收获（面试表达）

通过本项目，我重点理解了三个安全问题：

1. 输入与执行的边界问题（SQL注入）
2. 前端输出与脚本执行问题（XSS）
3. 攻击者视角下的请求可控性（Burp抓包分析）

在实践过程中，我逐步从“复现漏洞”转向“理解漏洞产生原因”，
并开始关注系统在设计层面的安全缺陷。
## ❓ 八、可能的面试讨论方向

在交流中可能涉及以下技术点：

- SQL注入的成因与防护方式
- XSS的不同类型及影响范围
- Burp Suite在渗透测试中的作用
- HTTP请求结构与参数控制方式
- 常见Web漏洞的基本防御思路
## 🚀 九、总结

本项目主要用于验证基础Web安全漏洞的形成原因与攻击方式，
帮助建立对常见Web安全问题的整体认知。

后续计划进一步学习：
- 更复杂的业务逻辑漏洞
- 权限控制类漏洞
- 企业级安全防护机制
