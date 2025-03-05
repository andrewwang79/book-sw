# 鉴权授权
> 统一身份身份认证（Authentication）和授权（Authorization）

## 概念
| 项 | 说明 |
| - | - |
| 身份访问管理IAM(Identity Access Manager) | 涵盖所有与访问身份验证相关的策略和工具的总称，包含对所有用户访问进行身份验证和授权。确保用户的访问权限授予是基于其工作角色和组织的。 |
| 特权访问管理PAM(Privileged Access Management) | 包含管理特权账户的安全所需的解决方案和工具，控制和监管和保护具有特权访问权限的用户。是IAM的子集 |
| 特权帐户管理(Privileged Account Management) | 是PAM的子集，专注于管理和组织帐户 |
| IDM(Identity Manager) | 身份管理 |
| [单点登录](https://blog.csdn.net/aboy123/article/details/35810867)SSO(Single Sign On) | 会话和用户**认证服务** <br> 单点登录：SSO（Single Sign On）<br> 中央认证服务：CAS（Central Authentication Service） |
| SSO帐号 | 主帐号：登录统一身份认证系统的帐号。从帐号：应用系统的登录帐号 |
| OAuth | 开放认证方式，第三方应用在用户授权的前提下访问用户在服务商存储的各种信息资源，无需用户名和密码 |
| SAML | 基于XML格式的**开放标准** |
| [JWT(JSON WEB Token)](https://juejin.im/entry/5993a030f265da24941202c2) |  |

## SSO VS OAuth
| 项 | 用途 | 使用场景 | 流程 | 示例 |
| - | - | - | - | - |
| SSO | 身份认证 | 企业或多个相关应用之间的无缝登录体验。用户只需登录1次就能访问多个相关的应用程序，而无需重复输入凭据。 | SSO服务生成全局的身份认证令牌，用户通过令牌登录不同服务，服务通过SSO服务验证令牌。 | 企业内部的应用，如办公套件、邮件系统和项目管理工具 | - |
| OAuth | 授权 | 在不同服务之间安全地共享资源，尤其是在陌生人网络中。 | 授权服务生成访问令牌，允许第三方应用在用户授权的范围和时间内访问资源服务获取用户资源（如社交媒体信息、文件存储等）。 | 使用Google或Facebook账户登录其他网站，授权第三方应用访问用户的基本信息。 | - |

这两者可以结合使用。例如在企业环境中，SSO可以用于内部的身份认证，OAuth可以用于授权用户访问外部服务的资源。

## SSO
| 种类 | 说明 |
| - | - |
| MSAD(Microsoft Active Directory) | 微软为Windows域网络开发的目录服务。 |
| OIDC(OpenID Connect) | 基于OAuth2.0，适用于现代Web应用和移动应用，提供简单的身份认证和用户信息获取方法。 |
| SAML2.0 | 适用于企业级单点登录（SSO）解决方案，支持复杂的跨域认证和授权需求。 |

### MSAD
* 是对网络中所有用户和计算机进行
    1. 身份验证和授权
    1. 分配和强制执行安全策略，比如用户登录、软件安装和更新等。

| 种类 | 说明 |
| - | - |
| LDAP（Lightweight Directory Access Protocol/轻量级目录访问协议） | 客户端用来与AD通信的协议，用于目录服务 |
| Kerberos | 基于AD域的客户端单点认证的授权协议，用于验证用户或主机的身份 |

### SAML2.0

## OAuth2.0
* 协议核心：用户提供1个令牌给第三方网站，1个令牌对应1个特定的第三方网站，同时该令牌只能在特定的时间内访问特定的资源
* 有授权服务和资源服务