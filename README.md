# User KiCad Footprints（KiCad用户封装库）

## 创立原因
- 由于合并请求提交后，需要一段时间来等待管理员审核通过，并且在这一期间内，根仓库中不含有新增的封装，所以我创立了该项目。

## 目的
- 统计并管理那些已经提交、并且还未被审核员批准通过的合并请求。

## 库存放位置
- 这些库应该放到KiCad的用户库路径下，并且添加软件内的索引路径。

    备注：如果找不到用户库路径，请参见[KiCad官网帮助页面](https://docs.kicad.org/8.0/zh/getting_started_in_kicad/getting_started_in_kicad.html) 寻找答案。

## 命名规则
- [√] 封装命名：完全遵循KiCad封装库命名规范，并且经过klc-check校验。
- [√] 封装库命名：在复制（复制将要与目标库合并的源库到用户库路径下）后的命名最前端增加“User_”字符串。

## 生命周期
1. 当合并请求被管理员审核通过、并且该封装库新增符号已经被添加进根封装库后，本项目内的对应用户封装库将会被删除。
2. 而后，用户应手动删除KiCad的用户库路径下的对应封装库。
3. 最终，从[KiCad封装库项目](https://gitlab.com/kicad/libraries/kicad-footprints)下载最新的根封装库并将软件本体的封装库覆盖。
