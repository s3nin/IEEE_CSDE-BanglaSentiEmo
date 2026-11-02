# IEEE_CSDE-BanglaSentiEmo
"BanglaSentiEmo" — shared BanglaBERT encoder for joint Bengali sentiment (5-class) &amp; emotion (7-class) classification, with matched STL baselines and five-seed diagnostic evaluation (IEEE CSDE 2026).
BanglaSentiEmo
Official implementation of the IEEE CSDE 2026 paper:
"BanglaSentiEmo: Diagnosing Cross-Task Affective Structure and Transfer with a Shared BanglaBERT Encoder for Bengali Sentiment-Emotion Classification"

Key finding: Bengali sentiment and emotion labels are strongly associated (Cramér's V ≈ 0.68), but a hard-parameter-sharing BanglaBERT model shows no statistically significant macro-F1 advantage over matched single-task models (exact paired permutation tests, p = 0.5625 and p = 0.8750). Strong task relatedness does not guarantee positive multi-task transfer. The shared encoder does, however, reduce parameters by 49.9%.


