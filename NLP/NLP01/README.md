# Attention 기반 Seq2Seq 한국어-영어 번역 모델

## 프로젝트 개요
- 한국어 → 영어 번역 모델
- Attention Seq2Seq 구조
- 최종 Loss: 0.0001
- 파라미터: 4,314,148

## 모델 구조
- **Encoder**: Bidirectional LSTM (2층, 256 hidden)
- **Attention**: Bahdanau Attention
- **Decoder**: LSTM with Attention (2층, 256 hidden)
- **Embedding**: 128 차원

## 데이터
- 학습 데이터: 360 문장
- 한국어 단어: 32 개
- 영어 단어: 36 개

## 번역 결과
```
E1) obama is the president <end>
E2) citizens live in the city <end>
E3) coffee is not needed <end>
E4) seven casualties have occurred <end>
```

## 학습 곡선
![Loss](training_loss.png)

## 실행 방법
```bash
pip install torch numpy matplotlib seaborn
python translation_model.py
```