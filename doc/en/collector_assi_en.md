# 自动采集辅助

## 注意：该功能处于测试阶段。出现任何问题，欢迎提交issue或直接反馈。提交时应提供Log日志文件，最好能够提供图片或视频。Thanks♪(･ω･)ﾉ

## 简介

自动采集辅助能够自动获取大部分提瓦特世界中的材料，例如可采集物，战利品等。

例子：自动采集甜甜花、琉璃百合，自动刷史莱姆、愚人众（高练度要求）。

本功能集成了自动战斗辅助，自动移动辅助，拾取辅助。在使用前，请确保已经阅读有关它们的配置信息。

## 快速开始

在GUI或config文件夹的auto_collector/common.json 文件中设置基本参数。

从GUI界面启动自动采集。

## 参数设置

- 推荐在GUI中编辑

| key         | item             |
|-------------|------------------|
| collection_name        | 需要采集的物品名称             |
| collection_type          | 采集的物品类型，分为`COLLECTION`（一般采集物）和`ENEMY`（战斗掉落物）         |

## 采集日志

采集日志(collection_log.json)是自动采集辅助产生的日志文件，包括：

| key         | item             |
|-------------|------------------|
| time        | 采集时间             |
| id          | 该类型掉落物id         |
| error_code  | 退出原因             |
| picked item | 在该次采集过程中采集到的所有物品 |


## 已采集地点

已采集地点(collected.json)保存了采集过的物品的id。

自动采集辅助会自动忽略这些地点。删掉即可恢复。

## 黑名单设置

在对应项的列表中加入id即可屏蔽这些采集项。

如果有些id的采集常常失败，可以加入黑名单，在下次采集时将会自动跳过。