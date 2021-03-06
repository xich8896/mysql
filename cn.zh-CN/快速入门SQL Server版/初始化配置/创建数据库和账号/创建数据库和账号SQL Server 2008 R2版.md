# 创建数据库和账号SQL Server 2008 R2版 {#concept_n3n_1zz_vdb .concept}

本文仅适用于SQL Server 2008 R2版本的实例。关于如何在SQL Server 2012版本的实例中创建数据库和账号，请参见文档[创建数据库和账号SQL Server 2012及以上版本](cn.zh-CN/快速入门SQL Server版/初始化配置/创建数据库和账号/创建数据库和账号SQL Server 2012及以上版本.md#)。

若要使用云数据库RDS，您需要在实例中创建数据库和账号。对于SQL Server 2008 R2版本的实例，您可以直接通过RDS控制台创建和管理实例的数据库和账号。本文将主要介绍在SQL Server 2008 R2版本的实例中创建数据库和账号的操作步骤。

## 背景信息 {#section_uv4_c11_wdb .section}

-   同一实例下的数据库共享该实例下的所有资源，每个SQL Server 2008 R2版本的实例最多可以创建50个数据库和500个账号。

-   如果您要迁移本地数据库到RDS，请在RDS实例中创建与本地数据库一致的迁移账号和数据库。

-   分配数据库账号权限时，请按最小权限原则和业务角色创建账号，并合理分配只读和读写权限。必要时可以把数据库账号和数据库拆分成更小粒度，使每个数据库账号只能访问其业务之内的数据。如果不需要数据库写入操作，请分配只读权限。

-   为保障数据库的安全，请将数据库账号的密码设置为强密码，并定期更换。


## 操作步骤 { .section}

1.  登录[RDS管理控制台](https://rds.console.aliyun.com/)。
2.  选择目标实例所在地域。
3.  单击目标实例的ID，进入基本信息页面。
4.  在左侧导航栏中选择的**账号管理**，进入账号管理页面。
5.  单击**创建账号**，如下图所示。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/7838/2761_zh-CN.png)

6.  输入要创建的账号信息，如下图所示。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/7838/2762_zh-CN.png)

    参数说明：

    -   数据库账号：账号名称，长度为2~16个字符，由小写字母、数字或下划线组成，但开头需为字母，结尾需为字母或数字。

    -   授权数据库：该账号授权的数据库，若尚未创建数据库，该值可以为空。一个账号可以授权多个数据库，授权数据库的操作步骤如下：

        1.  在未授权数据库栏中，选中要授权的数据库。
        2.  单击**授权**，将其添加数据库到已授权数据库栏中。
        3.  对于每个数据库，您可以选择该账号所拥有的权限，可选择****读写****或者**只读**。若对于所有授权数据库，该账号都具有相同的权限，您可以批量设置，请单击**全部设读写**或**全部设只读**，如下图所示。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/7838/2763_zh-CN.png)

    -   密码：该账号对应的密码，长度为8~32个字符，由大写字母、小写字母、数字、特殊字符中的任意三种组成。

    -   确认密码：输入与密码一致的字段，以确保密码正确输入。

    -   备注说明：可以备注该账号的相关信息，便于后续账号管理，最多支持256个英文字符。

7.  单击**确定**，账号创建完成。
8.  在左侧导航栏中选择**数据库管理**，进入数据库管理页面。
9.  单击**创建数据库**，如下图所示。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/7838/2764_zh-CN.png)

10. 输入要创建的数据库信息，如下图所示。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/7838/2765_zh-CN.png)

    参数说明：

    -   数据库\(DB\)名称：长度为2~64个字符，由小写字母、数字、下划线或中划线组成，但开头需为字母，结尾需为字母或数字。

    -   支持字符集：根据需要选择合适的字符集。

    -   授权账号：选中该数据库授权的账号，若尚未创建账号，该值可以为空。

    -   账号类型：选择授权账号后可见，设置该数据库授权给授权账号的权限，可选择**读写**或者**只读**。

    -   备注说明：可以备注该数据库的相关信息，便于后续数据库管理，最多支持256个英文字符。

11. 单击**确定**，数据库创建完成。

