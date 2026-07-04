# XSS漏洞（面试精简版）

## 本质
前端未做输入输出转义 → JS代码被执行

## 类型
- Stored XSS（存储型）
- Reflected XSS（反射型）

## Payload
```html
<script>alert(1)</script>
```

## 防御
- HTML转义
- CSP
- HttpOnly Cookie
