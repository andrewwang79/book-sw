# 测试
* 测试目标：不是找bug，而是确保质量
* 质量保证方法：覆盖率

## 概念术语
| 名称 | 英文 | 说明 |
| --  | -- | - |
| 测试用例 | TestCase | 有类型区别 |
| 测试用例集 | TestCaseSuite | 由测试用例组成，用于不同的测试目标。如每天测试，回归测试，性能测试，压力测试 |
| 测试报告 | TestReport | 由测试用例集组成，有对应的bug列表 |
| 缺陷 | Bug |  |  |

## 测试类型
### 功能测试
| 测试 | 英文 | 说明 |
| - | - | - |
| 验收测试 | UAT(Acceptance Testing) | 软件需求规格说明书 <br/> 验证产品是否满足用户的核心诉求，由产品/客户主导，属于用户视角的端到端验证 |
| 系统测试 | System Testing | 系统需求规格说明书。重点是使用场景 |
| 集成测试 | Integration Testing | 验证不同组件(模块间/软硬件)的的协同逻辑 |
| 接口测试 | Interface Testing | 验证接口的输入输出、异常响应 |
| 单元测试 | Unit Testing | 最小可测试单元：类、方法或者函数。重点是逻辑分支 |

* 系统测试的模式

| 测试 | 适用场景 | 说明 |
| - | - | - |
| 冒烟测试(Smoke Testing) | 构建后 | 核心业务的正向流程验证 <br/> 快速判断系统是否具备基本可测性 |
| 回归测试(Regression Testing) | 代码修改后 | 验证修改部分是否引入新问题 <br/> 覆盖修改模块及关联模块 <br/> 优先自动化执行历史用例 |

### 非功能测试
| 测试 | 英文 | 说明 |
| - | - | - |
| 性能测试 | Performance Testing |  |
| 负载测试 | Load Testing |  |
| 压力测试 | Stress Testing |  |
| 容量测试 | Volume Testing |  |
| 安全测试 | Security Testing |  |
| 兼容性测试 | Compatibility Testing |  |
| 安装测试 | Install Testing |  |
| 恢复测试 | Recovery Testing |  |
| 可靠性测试 | Reliability Testing |  |
| 可用性测试 | Usability Testing | 可用易用 |
| 一致性测试 | Compliance Testing |  |
| 本地化测试 | Localization Testing |  |

## 测试用例
### 来源
| 对比维度 | 产品需求驱动的测试用例 | 系统需求驱动的测试用例 |
| - | - | - |
| 测试目标 | 面向用户的业务需求、功能价值、使用场景 | 面向研发的技术实现、接口协议、性能指标 |
| 测试类型 | 系统测试、验收测试 | 单元测试、集成测试、接口测试、系统测试 |
| 测试内容 | 1. 功能场景的完整性：用户注册 -> 登录 -> 下单的全流程 <br/> 2. 业务规则的正确性：会员折扣计算等 <br/> 3. 可用性：易用性、兼容性 | 1. 接口参数的合法性：入参格式、必填项校验等 <br/> 2. 性能指标：响应时间≤1ms、并发用户数≥100等 <br/> 3. 非功能需求：安全性、稳定性、可扩展性等 |

### 可追溯
* 每个测试用例都需对应到至少一个需求点（产品需求或系统需求），形成需求 -> 测试用例 -> 缺陷的可追溯链路，避免测试遗漏。

### 分析方法
* [测试用例分析方法](https://blog.csdn.net/qq_46311811/article/details/122518205)，适用于白盒和黑盒测试。资料里更多是白盒测试示例。重点是以下两种测试方法：
    1. 等价类测试：输入输出测试用例
    1. 路径测试：分支测试用例
* 注意测试用例的复用性，不要因为小改动而要调整测试用例
* [软件测试用例模板（带实例）](https://wenku.baidu.com/view/37712285b9d528ea81c77939)

## 资料
* [软件测试方法——单元测试、集成测试、系统测试、确认测试](https://blog.csdn.net/u012426327/article/details/78400045)
* [单元测试、集成测试、系统测试和验收测试、冒烟测试、回归测试、随机测试、探索性测试和安全测试](https://juejin.im/post/6844903986462457864)
* [软件测试基础知识](http://wenku.baidu.com/view/388fdad0360cba1aa911da01.html)
* [软件测试类型](http://baike.baidu.com/item/%E8%BD%AF%E4%BB%B6%E6%B5%8B%E8%AF%95%E7%B1%BB%E5%9E%8B)
* [软件测试的16种测试类型](http://wenku.baidu.com/view/cac33c37eefdc8d376ee32ed.html)
* [bug优先级和严重级定义](http://blog.csdn.net/sunshine_mei/article/details/49230199)
* [阿里完整自动化测试解决方案macaca](https://yq.aliyun.com/articles/8310)
* [软件测试网](http://www.51testing.com/)

### 用户的测试级别
用户的测试级别有3级

| 级别 | 范围 | 说明 |
| - | - | - |
| 1 | 测试部门 |  |
| 2 | 公司内部 |  |
| 3 | 公司外部 |  |