# 超声六爪 · 手动联动机构

A 3D-printable, hand-actuated six-claw mechanism for an ultrasonic transducer array. One axial pushrod moves all six claws through matching curved slots.

这个仓库收录超声气泡操控课题的**六爪机械改造原型**。六组相同的爪指沿周向排列，推杆和导向筒相对移动时，爪指圆柱凸起沿圆弧槽滑动，带动六爪同步开合。圆弧槽的两端限制行程。

[查看分步装配及开合演示](media/assembly.gif)

## 文件

- [SolidWorks 源文件](cad/solidworks/) · SolidWorks 2025 保存的装配体和四种零件。下载整个文件夹，在同一目录内打开 `机械爪_手握杆140_圆盘10.SLDASM`。
- [STEP 零件](cad/step/) · 四种零件的独立实体，可在其他 CAD 中打开。
- [打印 STL](print/) · 四个零件文件，导入切片软件时按 **毫米** 解释。

| 打印件 | STL | 数量 |
| --- | --- | ---: |
| 双侧凸起爪指 | [claw.stl](print/claw.stl) | 6 |
| 支架与 140 mm 推杆 | [pushrod-140mm.stl](print/pushrod-140mm.stl) | 1 |
| 带限位圆弧槽的导向筒 | [slotted-guide.stl](print/slotted-guide.stl) | 1 |
| 10 mm 厚杆端圆盘 | [end-disc-10mm.stl](print/end-disc-10mm.stl) | 1 |

## 打印与装配

1. 原型使用 PLA，带槽导向筒打印时轴线竖直。拆支撑后检查槽口、凸起和导向孔，清理毛刺，再量实物尺寸。
2. 支架推杆先穿入导向筒。爪指的两侧凸起对准对应槽口，逐个干配。支架和爪指的铰接可用轴肩螺钉，之前的选型参考是光杆直径 Ø10 mm、光杆长度 20 mm。按打印件试配，让光杆覆盖转动孔，并留出轴向活动余量。
3. 先检查杆筒是否能抽动，再逐爪检查入槽和同步开合。确认行程后，把独立圆盘胶接在筒外的杆端。

## 关键尺寸与验证

| 部位 | CAD 名义尺寸 |
| --- | ---: |
| 槽宽 / 爪指凸起直径 | 10.6 / 9.8 mm |
| 导向孔 / 推杆直径 | 12.0 / 11.4 mm |
| 推杆拉伸长度 | 140 mm |
| 圆盘直径 / 厚度 | 33.7 / 10 mm |
| 轴向行程 | 约 11.1 mm |

最终版在五个离散开合位置做过 SolidWorks 几何干涉检查，抽查点均通过。实物试装仍观察到局部卡顿。槽销余量偏大时，同一杆位下六爪倾角也可能不同。复现时可在几个固定杆位检查实测间隙、六爪角差和推拉阻力，再决定是否调整配合。

## 许可

Copyright © 2026 BGrowl. 本仓库中的机械设计文件、打印模型和项目说明采用 [CERN Open Hardware Licence Version 2 – Permissive](LICENSE)，标识为 `CERN-OHL-P-2.0`。
