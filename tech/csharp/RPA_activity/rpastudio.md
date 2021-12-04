activity研究
描述
看一下怎么实现 加载自定义的 activity ，然后发挥出来
private void initAvailableActivities()
item.TypeOf = (activityNode as XmlElement).GetAttribute("TypeOf");//放在Icon赋值前面，因为Icon要借用TypeOf的信息
步骤
item.IsSystem = (activityNode as XmlElement).GetAttribute("IsSystem").ToLower() == "true";
\`\`\`
public RelayCommand SelectedItemInstallCommand
\`\`\`

## 資料

  RPAStudio.sln   

