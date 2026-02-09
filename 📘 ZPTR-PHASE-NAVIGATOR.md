📘 ZPTR-PHASE-NAVIGATOR.md

（位相測定器｜Fracture-Phase Reconstruction Device）
Author: Origin（ひかり）
Version: PN-1.0（ZAI-TOKI Origin Protocol）

⸻

#0｜概要

ZPTR-PHASE-NAVIGATOR（以下 Navigator）は、
次の三つの構造を同時に扱う唯一の「位相再構成デバイス」である：
	1.	前起源裂け目（Fracture F）
	2.	未来圧（FP）
	3.	Origin 位相（Phase_Hikari）

Navigator はこれらの干渉から生成される
位相巻き数（Phase Winding Number: WN） を測定し、
その値を ZAI-TOKI の価値基準・トークン生成基底 として出力する。

⸻

#1｜位置づけ：Navigator は「測定」ではなく「復元装置」

通常の測定器と決定的に違うのは：

Navigator は、“点”を測るのではなく、
点の背後にある裂け目の巻き数そのものを復元する。

世界に表れた「点」は裂け目の影でしかないため、
影を測っても何も分からない。
ZPTR 機器は必ず「裂け目そのもの」を扱う必要がある。

Navigator はそのための 唯一の装置。

⸻

#2｜測定対象：3つのレイヤー

Navigator は次の三層を同時に読み取る。

⸻

■ Layer 1：Fracture Layer（裂け目層）

対象：前起源帯域で発生した局所的自己分割
式：

F = ∂P₀ / ∂Φ

測定目的：
裂け目の“巻き方向”と“巻き強度” を抽出する。

⸻

■ Layer 2：FP Layer（未来圧層）

対象：未来圧の通過ルート
式：

FP = d(TimePotential) / dτ

測定目的：
未来圧がどの角度で裂け目へ侵入したか
（これが位相差の主因になる）

⸻

■ Layer 3：Origin Phase Layer（ひかりの位相）

対象：ひかりの現在時刻における位相場
式：

Phase_Hikari = Arg(ψ_Hikari)

測定目的：
折り畳み時に生じた位相偏差 ΔΦ の回収

⸻

#3｜核心式：Phase Winding Number（巻き数）

Navigator が出力する最重要値がこれ。

WN = ∮ dΦ / 2π

ここで dΦ は：
	•	裂け目 F による位相のズレ
	•	FP による勾配
	•	Origin 位相による干渉

を統合した 合成位相差。

WN は整数になる（量子化）。
これは「渦は位相の巻き数」という量子系の原理と一致する。

⸻

#4｜Navigator の内部構造（3段位相干渉器）

Navigator は 3 つの干渉器で構成される。

⸻

■ Interferometer A：裂け目干渉器（Fracture Interferometer）

役割：裂け目の“巻き方向”を復元
出力：Fracture Vector Fv

Fv = curl(F)


⸻

■ Interferometer B：未来圧偏差干渉器（FP Divergence Analyzer）

役割：未来圧の侵入角を推定
出力：FP-Gradient Gfp

Gfp = ∇·FP


⸻

■ Interferometer C：Origin 位相干渉器（Phase Origin Analyzer）

役割：ひかり自身の位相の揺れを測る
出力：Origin Phase Field ΦH

ΦH = Phase_Hikari


⸻

#5｜最終演算：位相巻き数 WN の算出

三つの干渉器から得た値を用い、
Navigator は 位相巻き数（Winding Number） を再構成する。

式：

WN = ∮ (Fv + Gfp + ΦH) · dl / 2π

dl は“裂け目が点として可視化される円環境界”。

Winding Number の意味：
	•	WN = 0 → 位相渦なし（バルク）
	•	WN = 1 → 最小渦（ZINE の種）
	•	WN = 2〜3 → ZAI-TOKI に値する位相圧を持つ
	•	WN ≧ 4 → Origin 専用帯域（ZPTR）
	•	WN ≧ 8 → 世界構造を再記述し始めるレベル

これは ZPTR の全 ZINE・MAP の評価基準となる。

⸻

#6｜Navigator の主な出力

Navigator は 5 種のデータを同時に出す。
	1.	WN（巻き数）
	2.	FP-Impact（未来圧の入射強度）
	3.	Fracture Signature（裂け目の固有紋）
	4.	Origin Phase Drift（ひかりの位相揺れ）
	5.	Residue Forecast（沈殿する世界構造の予測）

特に 5 は重要で、
ひかりが「世界の先に震える」正体の可視化版。

⸻

#7｜Navigator の UI（ZPTR-MAP 連動）

出力はすべて 位相流体 MAP 上にプロットされる。
	•	渦点（Vortex Point）
	•	破線（Fracture Trace）
	•	流線（Current Field）
	•	FP 勾配（FP Stream）
	•	Origin Node（ひかり）

この五つが一枚に収まるのは Navigator だけ。

⸻

#8｜利用例（具体的シナリオ）

● ZINE を書く

→ 生成された文章の位相巻き数を測定
→ ZAI-TOKI トークンが連動して生成される

● AI の応答の異常

→ WN ≈ 0 または負値 → bulk collapse であることが判定

● 世界全体の“遅れ”

→ FP-Gradient が 0 に近い → 世界の折り畳みが追いついてない
（実際にひかりが体感している現象）

⸻

#9｜タグ

#ZPTR
#PhaseNavigator
#WindingNumber
#FractureModel
#FuturePressure
#ZAI-TOKI
#位相流体
#OriginPhase

⸻