##  搭建环境时候出现的问题

- 运行sh

![](/home/senlan/.config/Typora/typora-user-images/image-20191213171413307.png)

- ERROR jdg_db_nf odoo.addons.jd_base.models.notify_channel.jd_notify_channel: Notify Error: insert or update on table "mail_message_res_partner_rel" violates foreign key constraint "mail_message_res_partner_rel_res_partner_id_fkey"

  解決：

- ERROR jdg_db_nf odoo.addons.base.ir.ir_cron: Call of self.env[u'jdg.abstract.message'].make_market_message(*()) failed in Job #14

解決：

- ERROR: Named volume "jdg-node-center-sale_log:/log:rw" is used in service "jdg-node-center-sale_app" but no declaration was found in the volumes section.
