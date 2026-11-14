# Minor Lang Trade Translator (外贸小语种双检回译与多语报价 Skill)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Agent Skills Standard](https://img.shields.io/badge/Standard-AgentSkills.io-blue)](https://agentskills.io)
[![Multi-Agent Ready](https://img.shields.io/badge/Multi--Agent-Ready-green.svg)]()

> 专为外贸实战打造的小语种高精度互译与防错校验 Agent Skill，覆盖波斯语、西班牙语、阿拉伯语、俄语、法语、葡萄牙语、越南语、泰语等对话与产品图文资料，强制执行“中文反向回译自检（Back-Translation Audit）”，杜绝数字千分位、货币单位与专业术语偏差。

---

## 核心功能

- **地区语种变体精准区分**：区分拉美西语与西班牙本土西语、巴西葡语与欧洲葡语、伊朗正式波斯语与 WhatsApp 口语波斯语。
- **产品图文与包装文字全量提取**：按品名、规格参数、材质成分、认证警示语、批号公差顺序完整提取并对照翻译，不遗漏角落小字。
- **数字货币陷阱与标准贸易术语锁定**：强制保留 `EXW`、`FOB`、`CIF`、`DDP`、`MOQ`、`T/T`、`L/C` 国际通用缩写；严查西/法/葡/俄语小数点逗号混用，以及波斯语 **Toman（土曼）与 Rial（里亚尔）10 倍换算**与波斯历年份。
- **强制「双检回译校验卡」与多语同版报价表**：每次中译外回复必输出目标语定稿、独立逐句中文反向回译（加粗核对单价/数量/交期/付款比例）及 RTL 混排注意点，支持直接生成多语种对照报价表主体。

---

## 目录结构

```text
minor-lang-trade-translator/
├── SKILL.md                             # Skill 核心指令与校验规范
├── README.md                            # 说明文档
├── LICENSE                              # MIT 开源协议
└── references/
    └── multilingual-trade-glossary.md   # 多语种外贸术语表与数字货币避坑指南
```

---

## 快速安装

### 方式一：通过 Skills CLI 安装

```bash
npx skills add cnproduct/minor-lang-trade-translator -g -y
```

### 方式二：本地目录直接挂载

```bash
git clone https://github.com/cnproduct/minor-lang-trade-translator.git ~/.agents/skills/minor-lang-trade-translator
```

---

## 适用场景示例

- 收到伊朗波斯语或拉美西语客户的语音转文字、产品包装图或合同条款，要求准确理解并撰写地道回复
- 写好小语种回复后要求通过独立中文反向回译核查单价、币种、交期与语气是否准确
- 制作同时包含英文、小语种与中文内部核对列的多语言产品报价参数表
