```python
# -*- coding: utf-8 -*-
{
    # 模块名称
    'name': "cmd_test",
    # 关键词
    'summary': """
        你好odoo，hello odoo""",
    # 模块说明
    'description': """
        Long description of module's purpose
    """,
    # 作者
    'author': "wangyifan",
    # 网站
    'website': "https://www.jianshu.com/u/2bcd2b8f9555",

    # Categories can be used to filter modules in modules listing
    # Check https://github.com/odoo/odoo/blob/master/odoo/addons/base/module/module_data.xml
    # for the full list
    # 类别
    'category': '军火交易',
    # 版本号
    'version': '0.1',


    # any module necessary for this one to work correctly
    # 本模块所依赖的模块，安装本模块会同时安装依赖的模块
    'depends': ['base'],


    # always loaded
    # 加载的处理文件，总是加载
    'data': [
        # 'security/ir.model.access.csv',
        'views/views.xml',
        'views/templates.xml',
    ],


    # only loaded in demonstration mode
    # 只加载演示模式 
    'demo': [
        'demo/demo.xml',
    ],
}
```

