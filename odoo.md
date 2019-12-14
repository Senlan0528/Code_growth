# ODOO

## 文件结构

![image-20191212141620797](/home/senlan/.config/Typora/typora-user-images/image-20191212141620797.png)

### 模型

#### 装饰器

- @api.multi
- @api.one
与 `api.multi` 装饰器类似，但是他将 `self` 处理成一条记录，也就是我们不需要对 `self` 进行循环处理
- @api.model
- @api.depends

函数在不使用这些装饰器时，默认 `self` 都是记录集，所以要记得对 `self` 进行循环处理。

### 视图

基本视图是以模型的ir.ui.view定义的，视图类型需要用arch字段来指定

```xml
<record model="ir.ui.view" id="view_id">
    <field name="name">view.name</field>
    <field name="model">object_name</field>
    <field name="priority" eval="16"/>
    <field name="arch" type="xml">
        <!-- view content: <form>, <tree>, <graph>, ... -->
    </field>
</record>
```

- form
- tree
- search

## 继承



## 权限分级

- 第一级是access rule，即表级权限，控制用户组对表的访问权限，一般是用`security/ir.model.access.csv`文件来管理

- 第二级是record rule，即行级权限，控制用户组对表中数据行的访问权限，可以写在`views/views.xml`文件中

  ```XMl
      <!--record 规则 -->
      <record id="rule_user_qingjia_qingjiadan" model="ir.rule">
        <field name="name">自己编辑自己的请假单</field>
        <field name="model_id" ref="model_qingjia_qingjiadan" />
        <field name="domain_force">[('create_uid','=',user.id)]</field>
        <field name="groups" eval="[(4,ref('base.group_user'))]"/>
      </record>
  ```

- 第三级是group rule，是字段级权限

  ```XML
  <button name="button_complete" states="confirm"
                      string="批准" type="workflow" class="oe_highlight"
                      groups="base.group_user"/>
  ```

