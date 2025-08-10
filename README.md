# AlphaFold3 Tutorial

[教程PDF-GitHub](slides.pdf) | [教程PDF-飞书](https://yihpch8rki.feishu.cn/wiki/LNjZwB0JUiFguVk32Pkc1vOUngb?from=from_copylink)

## PyMOL

- [下载PyMOL](https://pymol.org/2/)
- [申请License](https://www.pymol.org/edu/)
- [PyMOL wiki](https://pymolwiki.org/index.php/Main_Page)

## 在线使用AlphaFold3

- [AlphaFold3 Server](https://alphafoldserver.com/)

用PDB: 8BF8为例，运行AlphaFold3 Server，输入序列：

```
>8bf8_A
MIRNKAFVVRLYPNAAQTELINRTLGSARFVYNHFLARRIAAYLTYGQTSSELTLLKQAEETSWLSEVDK
FALQNSLKNLETAYKNFFRFPRFRKKRTGESYRTQFTNNNIQIGEGRLKLPKLGWVKTKGQQDIQGKILN
VTVRRIHEGHYEASVLCEVEIPYLPAAPKFAAGVDVGIKDFAIVTDGVRFKHEQNPKYYRSTLKRLRKAQ
QTLSRRKKGSARYGKAKTKLARIHKRIVNKRQDFLHKLTTSLVREYEIIGAGWGEFIRQLEYKAAWYGRL
VSKDRDENAALNIRREALVAAG
>8bf8_B
GUUGGUGGCUGCGGGAAUCUCAGACACCUUAAACGCUCAUGGAGGCUAUGUCAGACCUGGGCAAUGGUCU
GCGAAGUGAGAAUCACGCGACGUCGUGUGAGGUUCAAGAGU
```

## 本地部署AlphaFold3

- [AlphaFold3 GitHub](https://github.com/google-deepmind/alphafold3)
- [xFold (AlphaFold3 pytorch) from Shenggan](https://github.com/Shenggan/xfold)
- [Protenix from ByteDance](https://github.com/bytedance/Protenix)
- [Conda installation of AlphaFold3](https://github.com/pyDock/AlphaFold3-Conda-Install)

JSON 文件示例：

```json
{
    "dialect": "alphafold3",
    "version": 1,
    "name": "fastpet",
    "sequences": [
        {
            "protein": {
                "id": "A",
                "sequence": "TNPYARGPNPTAASLEASAGPFTVRSFTVSRPSGYGAGTVYYPTNAGGTVGAIAIVPGYTARQSSIKWWGPRLASHGFVVITIDTNSTLDQPESRSSQQMAALRQVASLNGTSSSPIYGKVDTARMGVMGWSMGGGGSLISAANNPSLKAAAPQAPWHSSTNFSSVTVPTLIFACENDSIAPVNSSALPIYDSMSQNAKQFLEIKGGSHSCANSGNSNQALIGKKGVAWMKRFMDNDTRYSTFACENPNSTAVSDFRTANC"
            }
        },
        {
            "ligand": {
                "id": "B",
                "smiles": "C1=CC(=CC=C1C(=O)O)C(=O)OCCCCOC(=O)C2=CC=C(C=C2)C(=O)OCCCCOC(=O)C3=CC=C(C=C3)C(=O)O"
            }
        }
    ],
    "modelSeeds": [
        42
    ]
}
```

`data.json` 文件示例：

```json
{
  "dialect": "alphafold3",
  "version": 2,
  "name": "fastpet",
  "sequences": [
    {
      "protein": {
        "id": "A",
        "sequence": "TNPYARGPNPTAASLEASAGPFTVRSFTVSRPSGYGAGTVYYPTNAGGTVGAIAIVPGYTARQSSIKWWGPRLASHGFVVITIDTNSTLDQPESRSSQQMAALRQVASLNGTSSSPIYGKVDTARMGVMGWSMGGGGSLISAANNPSLKAAAPQAPWHSSTNFSSVTVPTLIFACENDSIAPVNSSALPIYDSMSQNAKQFLEIKGGSHSCANSGNSNQALIGKKGVAWMKRFMDNDTRYSTFACENPNSTAVSDFRTANC",
        "modifications": [],
        "unpairedMsa": ""
        "pairedMsa": ""
        "templates": []
      }
    },
    {
      "ligand": {
        "id": "B",
        "smiles": "C1=CC(=CC=C1C(=O)O)C(=O)OCCCCOC(=O)C2=CC=C(C=C2)C(=O)OCCCCOC(=O)C3=CC=C(C=C3)C(=O)O"
      }
    }
  ],
  "modelSeeds": [
    42
  ],
  "bondedAtomPairs": null,
  "userCCD": null
}
```

## 蛋白功能注释

重要工具：[FoldSeek](https://search.foldseek.com/search)

从UniProt开始注释功能：

- 找到UniProt蛋白：[案例](https://www.uniprot.org/uniprotkb/P09546/entry#structure)




