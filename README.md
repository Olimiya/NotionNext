# NotionNext-Wiki

根据[原版本](https://github.com/tangly1024/NotionNext)进行修改。主要针对这个[issue](https://github.com/tangly1024/NotionNext/issues/1108)中提出的问题改进。

问题：
Notion端模板比较固定，使用单个数据库存。会丧失在Notion中写文章组织很多方便的地方。比如无限层级结构，随意嵌套，任意跳转和迅速索引。数据库中的文章不能通过目录栏快速索引。往往需要在写完文章后手动调整至NotionNext要求的模板中，强制要求为一级扁平结构。

改进方案：
Notion较新版本中已经添加了转换为wiki的功能。所以对于Notion写作后，直接将顶级页面转为wiki，然后公布这个页面的ID提供给NotionNext。这个用法对于Notion大部分功能就是无感的。转换为wiki后，同样会有一个包含所有page，以及相应的tag的一个页面。这样也能获得NotionNext所需要模板的所有信息。

## TODOs

1. 修改一份Wiki版本的Notion模板，维持原NotionNext中需要的所有结构。最小改动下，继续使用NotionNext，但支持Notion中大部分能力。
2. 逐步迁移一些博客文章到Notion中，使用NotionNext进行展示。记录痛点问题。
3. 解决元信息页面，比如菜单等的迁移冲突。最小化这部分信息需要的信息。
4. 构建一个原树状结构信息，取代原本的Category分类，添加一个新的层级结构的索引显示界面。
5. 扫描文章原本的内容，主要是对上层次的page，即在Notion下还包含子页面的，这些页面可单独设置一个属性Collection。对其中包含子页面的链接进行替换，替换为待article的普通post链接。目前应该也会替换，但是不作为一个post显示。