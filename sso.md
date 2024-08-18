# 单点登录集成
* 统一身份身份认证（Authentication）和授权（Authorization）

## 术语
| 项 | 说明 |
| - | - |
| SSO(Single Sign On) | 单点登录 |
| IAM(Identity Access Manager) | 统一身份认证系统 |
| IDM(Identity Manager) | 身份管理 |
| 帐号 | 主帐号：登录统一身份认证系统的帐号。从帐号：应用系统的登录帐号 |

## 种类
1. MSAD
1. OIDC(OpenID Connect)：基于OAuth2.0，适用于现代Web应用和移动应用，提供简单的身份认证和用户信息获取方法。
1. SAML 2.0：适用于企业级单点登录（SSO）解决方案，支持复杂的跨域认证和授权需求。

## MSAD(Microsoft Active Directory)
* 微软为Windows域网络开发的目录服务。主要作用是对网络中所有用户和计算机进行：
  1. 身份验证和授权
  1. 分配和强制执行安全策略，比如用户登录、软件安装和更新等。

| 项 | 说明 |
| - | - |
| LDAP（Lightweight Directory Access Protocol/轻量级目录访问协议） | 客户端用来与AD通信的协议，用于目录服务 |
| Kerberos | 基于AD域的客户端单点认证的授权协议，用于验证用户或主机的身份 |

## OAuth2.0
> 开放认证方式，第三方应用在用户授权的前提下访问在用户在服务商那里存储的各种信息资源(无需获取用户名和密码)
> API接口为主

* 协议核心：用户提供1个令牌给第三方网站，1个令牌对应1个特定的第三方网站，同时该令牌只能在特定的时间内访问特定的资源

## SAML2.0
