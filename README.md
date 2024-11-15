# gorm4gaussdb

[GORM](https://gorm.io) 是一个强大的Go编程语言中的ORM库，具有简单易用、多数据库支持、自动迁移、事务支持和强大的查询功能等特点。

[云数据库 GaussDB](https://support.huaweicloud.com/gaussdb/index.html) 是华为自主创新研发的分布式关系型数据库。该产品具备企业级复杂事务混合负载能力，同时支持分布式事务，同城跨AZ部署，数据0丢失，支持1000+的扩展能力，PB级海量存储。同时拥有云上高可用，高可靠，高安全，弹性伸缩，一键部署，快速备份恢复，监控告警等关键能力。

本项目的目的是让 GORM 支持华为云数据库 GaussDB。[开源软件 for Huawei 之 GORM 操作华为云数据库 GaussDB 攻略【最终章】](https://bbs.huaweicloud.com/blogs/439075)


## Quick Start

```go
import (
  gaussdb "github.com/okyer/gorm4gaussdb"
  "gorm.io/gorm"
)

dsn := "host=127.0.0.1 user=test password=123456 dbname=test port=8000 sslmode=disable TimeZone=Asia/Shanghai"
db, err := gorm.Open(gaussdb.Open(dsn), &gorm.Config{})
if err != nil {
    panic(err)
}
// TODO...
```

[examples](https://github.com/okyer/examples)

Checkout [https://gorm.io](https://gorm.io) for details.



