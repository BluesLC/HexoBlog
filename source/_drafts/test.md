---
title: test
url: 197.html
id: 197
categories:
  - 未分类
tags:
---

页面标签
----

内置的页面标签，实际上是动态生成的aspx文件要继承的类，这些变量与方法只允许对应的模板页面使用。位于DTcms.Web.UI项目的Page目录下，如果开发者需要增加一个页面可以在此目录中增加对应的继承类文件。

一、频道页面变量与方法
-----------

频道页面的内置变量与方法，只允许当前对应的频道模板页使用，其它模板页面无法使用。

1.1 频道列表页内置变量
-------------

所有频道列表页都继承此类，位于DTcms.Web.UI/Page/article_list.cs文件类。 **参数说明：** page：当前页码，int类型 category_id：类别ID，int类型 totalcount：数据总数，int类型 pagelist：分页页码字符串，string类型

1.2 频道详细页变量与方法
--------------

所有频道详细页都继承此类，位于DTcms.Web.UI/Page/article_show.cs文件类。

1.3 页面内置变量
----------

**参数说明：** id：当前文章ID，int类型 page：当前文章的调用别名，string类型 model：文章实体类，DTcms.Model.article类型

1.3.1 获取上一条下一条的A链接方法
--------------------

**参数说明：** urlkey： URL配置名称，string类型 type： -1代表上一条，1代表下一条 defaultvalue： 默认文本 callIndex： 是否使用别名做为链接，0使用ID，1使用别名 `get_prevandnext_article(urlkey, type, defaultvalue, callIndex)`

    <!--示例一：当前URL配置名称为news_show，显示上一条文章链接-->
    上一条：<%=get_prevandnext_article("news_show", -1, "没有啦！", 0)%>
    
    <!--示例二：当前URL配置名称为news_show，显示下一条文章链接-->
     下一条：<%=get_prevandnext_article("news_show", 1, "没有啦！", 0)%>

二、类别页面变量与方法
-----------

所有频道类别列表页都继承此类，位于DTcms.Web.UI/Page/category.cs文件类。

2.1 类别列表页内置变量
-------------

**参数说明：** category_id：父类别ID，0代表顶级分类，int类型

三、会员页面变量与方法
-----------

会员中心页面所继承的类，只允许对应的模板页访问。

3.1 会员中心页面内置变量
--------------

位于DTcms.Web.UI/Page/usercenter.cs文件类。 **参数说明：** action：操作类型，string类型 curr\_login\_ip：本次登录IP，string类型 pre\_login\_ip：上一次登录IP，string类型 pre\_login\_time：上一次登录时间，string类型 total\_order：未完成订单数量，int类型 total\_msg：未读短消息，int类型

3.2 会员金额记录页面内置变量
----------------

位于DTcms.Web.UI/Page/useramount.cs文件类。 **参数说明：** action：操作类型，string类型 page：当前页码，int类型 totalcount：总记录数，int类型

3.3 会员积分记录页面内置变量
----------------

位于DTcms.Web.UI/Page/userpoint.cs文件类。 **参数说明：** action：操作类型，string类型 page：当前页码，int类型 totalcount：总记录数，int类型

3.4 会员短消息列表页内置变量
----------------

位于DTcms.Web.UI/Page/usermessage.cs文件类。 **参数说明：** action：操作类型，string类型 page：当前页码，int类型 totalcount：总记录数，int类型

3.5 会员短消息详细页内置变量
----------------

位于DTcms.Web.UI/Page/usermessage_show.cs文件类。 **参数说明：** id：当前短消息的ID，int类型 model：当前短消息实体，DTcms.Model.user_message类型

3.6 会员订单列表页内置变量
---------------

位于DTcms.Web.UI/Page/userorder.cs文件类。 **参数说明：** action：操作类型，string类型 page：当前页码，int类型 totalcount：总记录数，int类型

3.7 会员订单详细页内置变量
---------------

位于DTcms.Web.UI/Page/userorder_show.cs文件类。 **参数说明：** id：当前订单的ID，int类型 model：当前订单实体，DTcms.Model.orders类型 payModel：支付方式实体，DTcms.Model.payment类型