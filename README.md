# Garden Defense

A simple tower defense game built with `Python` and `pygame`. Players plant sunflowers and pea shooters to defend the garden from incoming zombies, collect sunlight resources, and survive through increasingly difficult waves.

这是一个使用 `Python` 和 `pygame` 开发的植物大战僵尸风格小游戏项目。

## 设计思路

项目采用面向对象的方式组织游戏逻辑，将游戏中的地图、植物、子弹、僵尸和主程序分别封装成不同的类。

整体思路如下：

1. 使用 `pygame` 创建游戏窗口，并在主循环中不断刷新画面。
2. 将游戏区域划分为网格地图，每个格子记录是否可以种植植物。
3. 玩家通过鼠标操作种植植物：左键种植向日葵，右键种植豌豆射手。
4. 向日葵会定时产生阳光/金钱，作为继续种植植物的资源。
5. 豌豆射手会检测同一行是否存在僵尸，如果有僵尸就发射子弹。
6. 子弹向右移动，碰到僵尸后造成伤害，僵尸血量归零后被移除并增加得分。
7. 僵尸从屏幕右侧生成并向左移动，碰到植物后停止移动并攻击植物。
8. 如果僵尸移动到屏幕最左侧，则游戏结束。
9. 游戏根据得分推进关卡，并逐步调整僵尸生成节奏。

通过这种设计，游戏的各个对象职责清晰，方便后续继续扩展新的植物、僵尸、关卡和道具。

## 运行项目

```bash
conda activate plants
cd /Users/baihuiye/Desktop/Code/plants
python game.py
```
