






<p align="center">
  <!-- ===== Links ===== -->
  <a href="https://bin-cao.github.io/PyWPEM/">
    <img src="https://img.shields.io/badge/Homepage-プロジェクト-black?style=for-the-badge" />
  </a>

  <a href="https://pyxplore.netlify.app/">
    <img src="https://img.shields.io/badge/Docs-ドキュメント-grey?style=for-the-badge" />
  </a>

  <a href="https://arxiv.org/abs/2602.16372">
    <img src="https://img.shields.io/badge/arXiv-論文-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white" />
  </a>

  <a href="https://www.researchgate.net/publication/400962382">
    <img src="https://img.shields.io/badge/Supplementary-資料-teal?style=for-the-badge" />
  </a>

  <a href="https://www.pepy.tech/projects/PyXplore">
    <img src="https://img.shields.io/badge/Downloads-統計-4CAF50?style=for-the-badge" />
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
  <strong>X線回折シミュレーション・解析およびAI駆動構造精密化のためのPythonツールキット</strong> 
</p>

<p align="center">
  <img width="600" src="https://github.com/user-attachments/assets/e37ee8c4-8bdd-4de0-b27e-2ce7270a8a07" />
</p>

**Bilibiliにて中国語のチュートリアル動画を公開しました：[リンク](https://www.bilibili.com/video/BV1xfRVBQEFv/?spm_id_from=333.337.search-card.all.click&vd_source=6b9872e6d30ffcbac3baf8965e05bab4)**


その他のツールとして、初期構造推定のための [XQueryer](https://github.com/Bin-Cao/XQueryer) や、結晶物性予測のための [PRDNet](https://github.com/Bin-Cao/PRDNet) があります。

⚠️⚠️⚠️ **現在、PyXplore の全機能をサポートするユーザーインターフェースを開発中です**（[UIリポジトリ](https://github.com/WPEM/PyxploreUI) を参照）。このUIでは、ユーザーはデータとパラメータを入力するだけで、対応する実行コードが自動生成されます。今後の更新にご期待ください。

コミュニティからの貢献を歓迎します。貢献者は**本論文に謝辞として記載**されます。主要機能への大きな貢献は、将来のWPEM次期バージョンに関する論文で**共著者**となる可能性があります。

---

## 概要

**[PyXplore](https://pyxplore.netlify.app/)** は、**X線回折（XRD）のシミュレーション、分解、定量解析、およびAI支援による構造精密化**のためのモジュール型Pythonフレームワークです。

以下を統合しています：

* 物理ベースの回折モデリング  
* EMベースのブラッグ最適化  
* 構造グラフの構築  
* 消滅則およびWyckoff解析  
* アモルファス相の定量評価  
* AI駆動の構造精密化  

本ツールキットは、材料解析およびAI for Science研究における再現可能な科学ワークフローの構築を目的として設計されています。

PyPIからインストールし、[依存関係を設定](https://github.com/Bin-Cao/PyWPEM/blob/main/INSTALL.md)してください：

```bash
pip install PyXplore
````

最新版へアップグレード：

```bash
pip install --upgrade PyXplore
```

---

## 主な機能

* **XRDシミュレーション**
  結晶構造情報に基づく高精度な回折パターン生成

* **ピーク分解と定量解析**
  WPEMに基づく分解および体積分率の算出

* **ブラッグ則最適化（EMフレームワーク）**
  期待値最大化法によるパラメータ推定

* **消滅則とWyckoff処理**
  対称性を考慮した前処理と構造フィルタリング

* **グラフベース構造表現**
  機械学習タスクのための結晶グラフ構築

* **アモルファス構造解析**
  RDFに基づく定量評価

* **マルチモーダル拡張**
  XASおよびXPS解析モジュールを統合

---

## アーキテクチャ概要

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

本設計は、**物理一貫性を保ったモジュール構造**を採用しており、単独実行およびパイプライン実行の両方に対応します。

---

## 図表

<p align="center">
  <img width="450" src="https://github.com/user-attachments/assets/da5bd320-3651-4223-b862-06fb5ce1f96a" />
</p>

<p align="center">
  <img width="700" src="https://github.com/user-attachments/assets/50b1aacc-6a4f-4b58-95fb-a4094da60055" />
</p>

---

## 参考文献

研究で **PyWPEM** を使用する場合、以下を引用してください：

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

## 貢献

コミュニティからの貢献を歓迎します。

* Issueによるバグ報告
* 新機能の提案
* プルリクエストの送信
* 学術共同研究のご相談

提出前に、コードの可読性、ドキュメントの明確性、科学的妥当性を確認してください。

---

## ライセンス

本プロジェクトはMITライセンスの下で公開されています。

学術利用・商用利用ともに自由です。
学術研究で使用する場合は、関連論文の引用をお願いします。

---

<table>
  <tr>
    <td width="160" align="center" valign="top">
      <img src="https://github.com/user-attachments/assets/7e77bd5a-42d6-45db-b8e6-2c82cac81b9d" width="140" style="border-radius: 50%;"/>
    </td>
    <td valign="top">
      <b>お問い合わせやサポートが必要な場合は、以下までご連絡ください：</b><br>
      📧 Email: <a href="mailto:bcao686@connect.hkust-gz.edu.cn">bcao686@connect.hkust-gz.edu.cn</a><br><br>
      Cao Bin は、<b>香港科技大学（広州）</b>の博士課程学生であり、 
      <a href="https://gbaaa.org.hk/en-us/article/67">張統一教授</a>の指導のもと研究を行っています。  
      研究分野は <b>AI for Science</b>、特に知能化された結晶構造解析と発見です。  
      詳細は <a href="https://bin-cao.github.io/">個人ホームページ</a>をご覧ください。
    </td>
  </tr>
</table>

