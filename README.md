# 증강 기법에 따른 자연어 생성 성능 비교 웹 애플리케이션

## 소개
이 프로젝트는 증강 기법에 따른 자연어 생성 성능 비교 웹 애플리케이션입니다.
기본 모델은 KoGPT2 모델을 사용합니다.

1. 증강 기법은 다음과 같습니다.
- Synonym Replacement : 단어를 비슷한 의미를 가진 단어로 대체
- Random Insertion : 단어를 문장 중간에 무작위로 삽입
- Random Swap : 단어를 문장 중간에 무작위로 교환
- Random Deletion : 단어를 문장 중간에 무작위로 삭제

2. 성능 지표는 다음과 같습니다.
- Perplexity : 모델의 복잡도를 측정하는 지표
- BLEU : 문장의 유사도를 측정하는 지표
- ROUGE : 문장의 유사도를 측정하는 지표
- METEOR : 문장의 유사도를 측정하는 지표
- CHRF : 문장의 유사도를 측정하는 지표

3. TSNE 시각화를 통해 데이터셋을 시각화합니다.
- 증강 데이터 셋과 기본 데이터 셋을 비교하여 증강 데이터셋의 신뢰도를 확인합니다.

4. 증강된 데이터셋 예시를 확인할 수 있으며, 증강된 데이터셋을 다운로드 받을 수 있습니다.

5. 증강된 데이터셋으로 fine-tuning된 모델을 통해 채팅을 주고받을 수 있습니다.

## 시작하기

### 필요 조건
- Python 3.7 이상
- Flask

### 설치 방법
1. 이 저장소를 클론합니다.  
```bash
git clone https://github.com/seyun0714/HW5.git
cd HW5
```

2. 필요한 패키지를 설치합니다.   
```bash
pip install -r requirements.txt
```

## 사용 방법
애플리케이션을 실행하려면 다음 명령어를 사용하세요:
```bash
python app.py
flask run
```

애플리케이션은 기본적으로 `http://localhost:5000`에서 실행됩니다.

## 주요 기능
- **홈페이지**: 기본 라우트로 접속 시 파일 업로드 페이지로 이동합니다.
- **파일 업로드**: 파일 업로드 페이지에서 파일을 업로드하고 대시보드로 이동합니다.
- **데이터셋 증강**: 업로드한 파일을 증강하여 데이터셋을 생성합니다.
- **대시보드**: 대시보드 페이지에서 데이터셋 증강 및 시각화 결과를 확인할 수 있습니다.
- **데이터셋 시각화**: perplexity, BLEU, ROUGE, METEOR, CHRF, TSNE 등을 시각화합니다.
- **데이터셋 다운로드**: 증강된 데이터셋을 다운로드합니다.
- **모델 테스트**: 증강된 데이터셋으로 fine-tuning된 모델을 통해 채팅을 주고받을 수 있습니다.

## 기술 스택
- **Frontend**: HTML, CSS, JavaScript, Bootstrap, d3.js
- **Backend**: Flask