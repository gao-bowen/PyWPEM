








<p align="center">
  <!-- ===== Links ===== -->
  <a href="https://bin-cao.github.io/PyWPEM/">
    <img src="https://img.shields.io/badge/Homepage-项目-black?style=for-the-badge" />
  </a>

  <a href="https://pyxplore.netlify.app/">
    <img src="https://img.shields.io/badge/Docs-文档-grey?style=for-the-badge" />
  </a>

  <a href="https://arxiv.org/abs/2602.16372">
    <img src="https://img.shields.io/badge/arXiv-论文-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white" />
  </a>

  <a href="https://www.researchgate.net/publication/400962382">
    <img src="https://img.shields.io/badge/Supplementary-补充材料-teal?style=for-the-badge" />
  </a>

  <a href="https://www.pepy.tech/projects/PyXplore">
    <img src="https://img.shields.io/badge/Downloads-下载量-4CAF50?style=for-the-badge" />
  </a>

</p>

<p align="center">

  <!-- ===== GitHub Stats ===== -->

  <a href="https://github.com/Bin-Cao/PyWPEM">
    <img src="https://img.shields.io/github/stars/Bin-Cao/PyWPEM?style=for-the-badge&logo=github" />
  </a>

  <a href="https://github.com/Bin-Cao/PyWPEM/forks">
    <img src="https://img.shields.io/github/forks/Bin-Cao/PyWPEM?style=for-the-badge&logo=github" />
  </a>

  <a href="https://github.com/Bin-Cao/PyWPEM/issues">
    <img src="https://img.shields.io/github/issues/Bin-Cao/PyWPEM?style=for-the-badge&logo=github" />
  </a>

  <a href="https://github.com/Bin-Cao/PyWPEM/issues?q=is%3Aissue+is%3Aclosed">
    <img src="https://img.shields.io/github/issues-closed/Bin-Cao/PyWPEM?style=for-the-badge&logo=github" />
  </a>

  <a href="https://github.com/Bin-Cao/PyWPEM/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/Bin-Cao/PyWPEM?style=for-the-badge" />
  </a>

  <a href="https://github.com/Bin-Cao/PyWPEM/commits/main">
    <img src="https://img.shields.io/github/last-commit/Bin-Cao/PyWPEM?style=for-the-badge" />
  </a>
</p>

<p align="center">
  <img src="https://github.com/Bin-Cao/TCGPR/assets/86995074/28f69830-4ece-43b3-a887-e78fdb25bcab" width="140" alt="PyWPEM Logo"/>
</p>

<p align="center">
  <strong>用于 X 射线衍射模拟、分析与 AI 驱动结构精修的 Python 工具包</strong> 
</p>

<p align="center">
  <img width="600" src="https://github.com/user-attachments/assets/e37ee8c4-8bdd-4de0-b27e-2ce7270a8a07" />
</p>

其他工具包括：[XQueryer](https://github.com/Bin-Cao/XQueryer)（用于初始结构推断）以及 [PRDNet](https://github.com/Bin-Cao/PRDNet)（用于晶体性质预测）。

⚠️⚠️⚠️ **我正在开发一个用户界面以支持 PyXplore 的全部功能**（参见 [UI 仓库](https://github.com/WPEM/PyxploreUI)）。通过该界面，用户只需输入数据与参数，即可自动生成对应的执行代码。敬请关注后续更新。

我们欢迎社区贡献。贡献者将会在当前论文中**致谢**。对关键功能的重要贡献可能在后续版本的 WPEM 论文中获得**共同作者**资格。

---

<p align="center">
  <a href="https://star-history.com/#Bin-Cao/PyWPEM&Date">
    <img 
      src="https://api.star-history.com/svg?repos=Bin-Cao/PyWPEM&type=Date" 
      width="650"
      style="border: 1px solid #d0d7de; border-radius: 12px; padding: 8px; background: #ffffff;"
    />
  </a>
</p>

---

## 概述

**[PyXplore](https://pyxplore.netlify.app/)** 是一个模块化的 Python 框架，用于 **X 射线衍射（XRD）模拟、分解、定量分析以及 AI 辅助结构精修**。

它集成了：

* 基于物理的衍射建模
* 基于 EM 的布拉格优化
* 结构图构建
* 消光与 Wyckoff 分析
* 非晶相定量分析
* AI 驱动结构精修

该工具包旨在支持材料表征与 AI for Science 研究中的可复现科学工作流。

---

从 PyPI 安装，并参考 [依赖安装说明](https://github.com/Bin-Cao/PyWPEM/blob/main/INSTALL.md)：

```bash
pip install PyXplore
```

升级到最新版本：

```bash
pip install --upgrade PyXplore
```

---

## 核心功能

* **XRD 模拟**
  基于晶体结构信息生成高精度衍射图谱。

* **峰分解与定量分析**
  基于 WPEM 方法进行分解与体积分数计算。

* **布拉格定律优化（EM 框架）**
  基于期望最大化算法进行参数求解。

* **消光与 Wyckoff 处理**
  支持对称性约束下的结构预处理与筛选。

* **基于图的结构表示**
  构建晶体图结构用于下游机器学习任务。

* **非晶结构分析**
  基于 RDF 的定量评估方法。

* **多模态扩展**
  集成 XAS 与 XPS 分析模块。

---

## 架构概览

```text
PyWPEM/
├── WPEM.py
├── XRDSimulation/
├── EMBraggOpt/
├── Refinement/
├── StructureOpt/
├── GraphStructure/
├── Extinction/
├── Amorphous/
├── Background/
├── Plot/
├── DecomposePlot/
├── WPEMXAS/
├── WPEMXPS/
└── refs/
```

该设计遵循**物理一致性与模块化架构**，支持独立执行或流水线式组合。

---

## 图表展示

<p align="center">
  <img width="450" src="https://github.com/user-attachments/assets/da5bd320-3651-4223-b862-06fb5ce1f96a" />
</p>

<p align="center">
  <img width="700" src="https://github.com/user-attachments/assets/50b1aacc-6a4f-4b58-95fb-a4094da60055" />
</p>

---

## 科学引用

如果您在研究中使用了 **PyWPEM**，请引用：

```bibtex
@article{cao2026wpem,
  title={AI-Driven Structure Refinement of X-ray Diffraction},
  author={Bin Cao, Qian Zhang, Zhenjie Feng, Taolue Zhang, Jiaqiang Huang, Lu-Tao Weng, Tong-Yi Zhang},
  journal={arXiv preprint},
  year={2026},
  url={https://arxiv.org/abs/2602.16372v1}
}
```

---

## 贡献

我们欢迎社区贡献：

* 通过 Issues 报告问题
* 提出新功能
* 提交 Pull Request
* 开展学术合作

提交前请确保代码可读性、文档清晰性以及科学正确性。

---

## 许可证

本项目基于 MIT License 发布。

可用于学术与商业用途，使用于科研时请引用相关论文。

---

<table>
  <tr>
    <td width="160" align="center" valign="top">
      <img src="https://github.com/user-attachments/assets/7e77bd5a-42d6-45db-b8e6-2c82cac81b9d" width="140" style="border-radius: 50%;"/>
    </td>
    <td valign="top">
      <b>如有任何问题或需要帮助，欢迎联系 CAO Bin：</b><br>
      📧 Email: <a href="mailto:bcao686@connect.hkust-gz.edu.cn">bcao686@connect.hkust-gz.edu.cn</a><br><br>
      Cao Bin 是 <b>香港科技大学（广州）</b> 博士研究生，
      师从 <a href="https://gbaaa.org.hk/en-us/article/67">Zhang Tong-Yi 教授</a>。
      其研究方向为 <b>AI for Science</b>，重点关注晶体结构智能解析与发现。
      更多信息请访问其
      <a href="https://bin-cao.github.io/">个人主页</a>。
    </td>
  </tr>
</table>
