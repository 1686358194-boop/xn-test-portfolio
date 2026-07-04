# xn-test｜Web安全渗透测试作品集（面试强化版）

## 👤 一、项目定位（面试开场30秒版本）
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

## 🧠 三、核心能力（HR筛选关键词）
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

## 💥 五、漏洞复现说明（面试重点）

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

#### 🔒 修复方式（面试必答）
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

## 🎤 七、面试讲解稿（重点！！）

### ⭐ 30秒版本
> 我这个项目是在DVWA靶场上做的Web安全漏洞复现，主要做了SQL注入和XSS攻击验证，同时使用Burp Suite进行抓包和请求重放。通过这个项目我理解了常见Web漏洞的成因、攻击方式以及基本防护思路。

---

### ⭐ 2分钟深入版本
> 在SQL注入部分，我通过构造 OR 1=1 和错误注入验证了数据库查询逻辑被绕过的问题，本质是后端未使用参数化查询导致的拼接漏洞。
>
> 在XSS部分，我分别验证了Stored和Reflected XSS，Stored类型会持久化存储恶意脚本，而Reflected通过URL即时执行。
>
> 同时我使用Burp Suite对HTTP请求进行拦截和修改，从而模拟攻击者视角分析系统漏洞。

---

## ❓ 八、面试官高频追问（提前准备）

### Q1：SQL注入怎么修？
👉 Prepared Statement + 参数绑定

### Q2：为什么XSS能偷Cookie？
👉 JS可访问document.cookie（无HttpOnly）

### Q3：Burp Suite你用来做什么？
👉 抓包 + 修改请求 + 重放验证

### Q4：你真实环境做过吗？
👉 强调：靶场验证 + 安全学习环境

---

## 🚀 九、总结一句话
👉 这是一个“从攻击视角理解Web安全基础漏洞”的实战项目
