---
title: "硬盘简介"
description: Test description
draft: false
enableToc: false
weight: 1
keyword: 山河，硬盘，SSD
---

## 产品概述

硬盘是 山河 shanhe 平台为云服务器提供的块存储设备，支持多种规格和类型，并可弹性扩展，可满足不同场景的业务需求，并且支持硬盘多副本及定时备份。

根据硬盘的创建方式及生命周期，硬盘可分为系统盘和数据盘。

- **系统盘**：系统盘用来存储云服务器运行的操作系统，随着云服务器的创建而自动创建，云服务器的删除而自动删除。系统盘在创建时将自动初始化，默认磁盘分区形式为主启动记录分区（MBR）。

- **数据盘**：数据盘用来存储数据，独立于云服务器的生命周期，可以在创建云服务器时创建，也可以单独创建，需要手动初始化后才能正常使用。

> **说明**：
>
> 系统盘只能使用本地盘；数据盘既可使用本地盘，也可使用云盘。
>
> 除特别指明外，文中所描述的硬盘相关内容（如硬盘购买与初始化）均是针对数据盘。

## 产品优势

- 规格丰富：支持多种类型及规格，满足您不同的业务场景及预算要求。
- 超高性能：增强型 SSD 硬盘，单盘 IO 性能可达10万 IOPS。
- 安全可靠：通过软件定义存储 SDS2.0 的功能，让您可以灵活的选择副本策略，数据可靠性达99.9999%；同时，业务正常运行时也可以进行在线备份，并可随时回滚，满足您各方面的使用需求。
- 弹性扩容：支持在线扩容，满足您不断变化的存储需求。
- 便捷易用：支持菜单界面和图形界面操作，并随时查看资源使用情况、操作日志等。

## 硬盘类型

<!--按照云硬盘性能及不同适用场景，青云QingCloud提供了四种类型的云硬盘：-->

<!--基础型：提供均衡的价格与性能，适用于数据不被经常访问、低I/O负载要求的应用。-->

<!--SSD企业型：采用全闪存架构，适用于对IOPS和吞吐要求很高的服务-->

<!--企业级分布式SAN：基于全闪存架构提供的分布式SAN服务，适用于对IOPS、吞吐、容量和稳定性要求很高的业务-->

<!--容量型：独立于云服务器生命周期，可以被连接到任意运行中的云服务器，适用于对容量要求较高的应用-->

<!--各类硬盘性能参数及适用场景如下：-->

山河 shanhe 向用户提供了云盘和本地盘两大类型硬盘。

- **云盘**：云服务器的块存储产品，采用多副本的分布式机制，具有低时延、高性能、持久性、高可靠等性能，可以随时创建或释放，也可以随时扩容。
- **本地盘**：云服务器所在物理机（宿主机）上的本地硬盘，具有低时延、高随机IOPS、高吞吐量、高性价比优势，但是本地盘的数据可靠性取决于物理服务器的可靠性，存在单点故障风险，使用本地盘的用户需要做好数据冗余，以保障数据的可用性。

</br>

**云盘类型**

目前，云盘类型包括：通用型SSD、容量型及增强型SSD。

| <span style="display:inline-block;width:90px">类型</span> | <span style="display:inline-block;width:110px">通用型SSD云盘</span> | <span style="display:inline-block;width:110px">容量型云盘</span> | 增强型SSD云盘                                          |
| --------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------ |
| 曾用名                                                    | 企业级分布式SAN（NeonSAN）                                   | 容量型硬盘                                                   | -                                                      |
| 容量                                                      | 20～24000 GB                                                 | 20～32000 GB                                                 | 450～32000 GB                                          |
| 区域及可用区                                              | 北京3区-B<br/>北京3区-C<br/>北京3区-D<br/>广东2区<br/>上海1区 <!--山河计算平台<br/>齐鲁工大计算平台--> | 北京3区-B<br/>北京3区-C<br/>北京3区-D<br/>广东2区<br/>上海1区<br/>雅加达区 <!--山河计算平台<br/>齐鲁工大计算平台--> | 北京3区-B<br>  <!--山河计算平台<br/>齐鲁工大计算平台-->     |
| 适用主机类型                                              | 所有                                                         | 所有                                                         | 所有                                                   |
| 单盘最大吞吐                                              | 350 MB/S                                                     | 150 MB/S                                                     | 750 MB/S                                               |
| 单盘吞吐性能                                              | min{128 + 0.5 * 容量, 350} MBps                              | min{100+0.15*容量, 150} MBps                                 | min{128 + 存储容量（GB）× 0.5,750} MBps                |
| 单盘最大IOPS                                              | 50000                                                        | 5500                                                         | 100000                                                 |
| 单盘IOPS性能                                              | min{2000 + 50 * 容量, 50000}                                 | min{1800 + 8 * 容量, 5500}                                   | min{2000 + 存储容量（GB）× 50,100000}                  |
| 时延                                                      | 0.3 ms                                                       | 0.5 ms                                                       | 0.05 ms                                                |
| 适用场景                                                  | 高性能，适合对吞吐和延时有一定要求的企业级场景               | 高性价比，适合中等性能要求的中小型建站等场景                 | 超高性能，适用分布式数据库等对IOPS和延时要求极高的服务 |

</br>

 **本地盘类型**

目前，本地盘类型包括：基础型和企业型SSD。

> **说明**：
>
> 基础型硬盘仅可作为基础型主机的系统盘或数据盘；企业型SSD硬盘既可作为系统盘，也可自行创建用作数据盘。

| <span style="display:inline-block;width:131px">类型</span> | 基础型本地盘                     | 企业型SSD本地盘                               |
| ---------------------------------------------------------- | -------------------------------- | --------------------------------------------- |
| 曾用名                                                     | 基础型硬盘                       | SSD企业级硬盘                                 |
| 容量                                                       | 10～2000 GB                      | 20～2000 GB                                   |
| 区域及可用区                                               | 除北京3区-A                      | 除北京3区-A                                   |
| 适用主机类型                                               | 基础型                           | 不能用在基础型主机及GPU主机                   |
| 单盘最大吞吐                                               | 100 MB/S                         | 320 MB/S                                      |
| 单盘吞吐性能                                               | min{36 + 0.15 * 容量, 100 } MBps | min{128 + 0.5 * 容量, 320} MBps               |
| 单盘最大IOPS                                               | 2500                             | 30000                                         |
| 单盘IOPS性能                                               | min{500 + 8 * 容量, 2500}        | min{2000 + 30 * 容量, 30000}                  |
| 时延                                                       | 0.2 ms                           | 0.2 ms                                        |
| 适用场景                                                   | 用作基础型主机的系统盘或数据盘           | 适合高吞吐低延时要求的I/O密集型应用、数据库等 |

</br>

**历史硬盘类型**

目前已不支持购买历史类型的硬盘，仅对以往购买过历史类型硬盘的老用户可见。

| <span style="display:inline-block;width:90px">类型</span> | 容量型（云盘）                               | <span style="display:inline-block;width:140px">性能型（本地盘）</span> | <span style="display:inline-block;width:200px">超高性能型（本地盘）</span> |
| --------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 容量                                                      | 20～5000 GB                                  | 20～2000 GB                                                  | 20～2000 GB                                                  |
| 区域及可用区                                              | 北京3区-A<br/>亚太区                         | 北京3区-A                                                    | 北京3区-A                                                    |
| 适用主机类型                                              | 所有                                         | 性能型主机                                                   | 超高性能型主机                                               |
| 单盘最大吞吐                                              | 36 MB/S                                      | 128 MB/S                                                     | 256 MB/S                                                     |
| 单盘最大IOPS                                              | 数百                                         | 5000                                                         | 25000                                                        |
| 时延                                                      | 毫秒级                                       | 毫秒级                                                       | 毫秒级                                                       |
| 适用场景                                                  | 高性价比，适合中等性能要求的中小型建站等场景 | 性能中等，适合个人建站等场景                                 | 高性能，适合企业级场景                                       |
