# SQL注入（面试精简版）

## 本质
SQL语句拼接导致逻辑可控

## Payload
```sql
1' OR 1=1 --
```

## 风险
- 绕过登录
- 数据泄露
- 报错信息暴露结构

## 防御
- Prepared Statement
- 参数化查询
