# ark-plugin

适用于Yunzai-Bot的全服排行插件，提供角色全服排行，多文件备份等功能

## 插件安装
```
git clone -b ark-plugin-alpha https://github.com/NotIvny/yunzai-characterRank-js.git ./plugins/ark-plugin
```
## 使用方法

安装后输入 #ark替换文件miao-rank ，重启后即可使用全部功能

### #xx排名 

最右侧新增角色全服排名(需#更新面板后才可显示)

### #xx面板 

伤害计算底部新增角色全服排名(需#更新面板后才可显示)

### #角色排名雷神uid 

手动获取角色排名

以上功能支持原神/星铁

使用 #xx排名 命令时，自动更新并获取角色排名

也可使用 #角色排名雷神uid 手动获取

示例：

#角色排名雷神\*\*\*\*\*\*\*\*\*

> uid:\*\*\*\*\*\*\*\*\*的雷电将军全服伤害排名为 459 / 718，伤害评分: \*\*.\*\*

#雷神排名

> uid:\*\*\*\*\*\*\*\*\*的雷电将军全服伤害排名为 459 / 718，伤害评分: \*\*.\*\*

*总排名

> uid:*********的星铁全服排名数据:<br>
瓦尔特全服伤害排名为37 / 110，伤害评分: 24.82<br>
希儿全服伤害排名为159 / 488，伤害评分: 56.94<br>
景元全服伤害排名为215 / 265，伤害评分: 22.14<br>
刃全服伤害排名为105 / 324，伤害评分: 39.65<br>
符玄全服伤害排名为251 / 468，伤害评分: 14.95<br>
藿藿全服伤害排名为205 / 302，伤害评分: 58.43<br>
阮•梅全服伤害排名为608 / 624，伤害评分: 8.24<br>
真理医生全服伤害排名为65 / 359，伤害评分: 36.78<br>
花火全服伤害排名为455 / 538，伤害评分: 37.91<br>

### #ark创建备份 
创建备份，需提供ID和以下两个文件夹路径：

src path: 替换用的文件所在的文件夹。

dest path: 被替换的文件所在的文件夹，即需要备份的文件所在的文件夹。

创建备份后，插件会自动获取src path下的所有文件名，并储存在backup.json中，以后仅这些文件会被替换。

同时, src path 的同目录下会创建一个以 backup 为后缀的文件夹，该文件夹将保存备份数据（接下来称 dest-backup path）。

为确保备份可用，建议您将替换用文件夹放在插件的backup文件夹，即指定src path在./plugins/ark-plugin/backup路径下。

注意: 与常规备份插件不同，本插件额外提供了一个"注入文件"的功能(src path => dest path)，以安全地修改插件代码，关系图如下所示。

src path => dest path <=> dest-backup path

于此同时，备份/替换的文件量不再由 dest path 决定，而是由 src path 决定。

因此，该功能适用于备份 JS、CSS、HTML 文件等固有文件，不适合备份数据文件。

### #ark替换文件

将 src path 中的文件替换到 dest path 中。

### #ark恢复文件

使用 dest-backup path 中的文件替换到 dest path 中。

## 其他
相关排名API可嵌入面板/排名图中

嵌入面板中效果：

![8a6b16deee772c4d66d0fdae278335b6](https://github.com/NotIvny/yunzai-characterRank-js/assets/125482125/68b37c47-4642-4e86-a9c0-fb55498646c7)
嵌入排名效果：

![5dda9bdbcfe9d6926a3e38aa1bcb0a87](https://github.com/NotIvny/yunzai-characterRank-js/assets/125482125/625de99f-8bf0-47b3-be2a-cc177650731b)

教程：
[custom.md](https://github.com/NotIvny/yunzai-characterRank-js/blob/main/custom.md)

全服排名数据源于用户更新面板，目前数据量在3000左右

当前插件正在快速迭代，由于js插件无法自动更新，请您及时手动更新

插件只会上传用户uid，不会上传其他信息

圣遗物排名、分段数据未来将更新

