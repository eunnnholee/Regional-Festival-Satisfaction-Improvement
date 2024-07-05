# 지역균형발전을위한 지역축제만족도개선연구 : 토픽 모델링과 QFD를 중심으로
> 토픽 모델링을 통해 도출된 키워드를 조합해 QFD의 “What List”와 “How List”를 작성한다. QFD 다이어그램을 작성함으로써 “What List”와 “How List” 가 축제에서 중요한 측면과 그것을 어떻게 달성할 지에 대한 관계를 나타낸다. QFD를 통해 산출한 중요도를 지역 축제 요구품질 중요도로 설정하여, 결과적으로 지역 축제의 만족도를 개선하고 본래의 문제점을 해결할 수 있도록 한다.
>  - QFD(Quality Function Deployment)는 제품이나 서비스의 설계 및 개발 과정에서 고객의 요구와 기대를 반영하여 품질을 향상시키기 위한 방법론이다. QFD는 고객의 목소리(Voice of Customer, VoC)를 체계적으로 수집하고 이를 설계, 생산, 서비스 등 각 단계에서 구체적인 요구사항으로 변환하는 프로세스를 포함한다. 주요 도구로는 ’품질의 집(House of Quality)’이 사용되며, 이는 고객의 요구사항과 이를 충족시키기 위한 기술적 요구사항을 매트릭스 형태로 시각화한 것이다.

</br>

## I. 프로젝트 개요

### 데이터셋: 
1. 우리나라 지역축제에 관한 많은 양의 데이터가 필요
  - NAVER, Daum 등의 국내 웹사이트 및 국내 웹사이트에서 운영하는 서비스

2. 지역축제에 대한 사실 정보보다는 의견, 감상도 포함된 데이터가 필요
  -  포털 기사(X)

3. 홍보글, 도배글 등 부적절한 데이터를 걸러내기 위해 어느 정도의 폐쇄성이 필요
  - Blog, Instagram(X): 글을 쓰는 데에 아무 제한이 없음.

> **Naver 대표 인기 카페 10곳 중 ‘축제’ 키워드를 검색해서 게시글 수가 가장 많은 카페 2개로 선정**
> - 자녀를 둔 가족 단위로 각 지역의 축제나 행사에 다니며, 카페를 통해 ‘지역축제’에 대한 정보를 공유 = ‘지역축제’에 대한 충분하고 적절한 데이터
> - 약 2500개의 개시글과 내용을 셀레니움을 통해 크롤링

</br>​

### 연구 배경:
> 현재 우리나라 전 지역에서 수도권 인구 집중화 현상을 완화하고, 지방의 경제를 활성화하는 것을 목적으로 한 ‘지역 축제’가 개최되고 있다. 하지만 정체성, 경쟁력 없는 행사들로 인해 본래의 목적과는 다르게 지방재정을 낭비하는 결과만을 초래해왔다. 이에 본 연구에서는 토픽모델링을 통해 ‘지역 축제’의 문제 속성이 무엇인지 파악하고, 해결하기 위한 요인을 도출하여, QFD에 적용하여 효과적인 대안을 수립하고자 한다.

</br>

### Research Question: 
> 토픽 모델링과 QFD를 활용하여 지역 축제의 문제점을 파악하고 해결하기 위한 효과적인 대안은 무엇인가?

</br>

### Literature Review:
1. 문지영, 김학선, 이종호. "의미연결망 분석을 활용한 음식관광 활성화 방안에 관한 연구.” (2020)
  > - 주제 : 텍스트 마이닝 & 지역 관광
  > - 리뷰 : ‘음식관광’을 중심으로 주요 키워드, 이슈가 무엇인지 빅데이터를 분석했을 때, ‘이벤트, 숙박, 사진, 여행, 지역, 축제’가 높은 빈도로 노출됨. CONCOR 분석으로 단어를 일반 관광 요소/시대적 특징을 갖는 요소/관광홍보대사와 관련된 요소로 나눌 수 있음.

2. 박지원, 이형룡. "관광지 만족도를 평가하는 관광지 선택속성에 관한 연구.” (2022)
  > - 주제 : 텍스트 마이닝 & 관광 속성
  > - 리뷰 : 관광지 선택속성을 도출하기 위해 특정 온라인 커뮤니티 리뷰 데이터를 활용하고 TF-IDF 토픽 모델링 기법을 제안한 것이 특징이다. 또한 LDA 토픽모델링의 결과를 FsQCA 분석으로 확장하여, 관광지 선택속성을 밝히는 것뿐만 아니라, 어떠한 관광지 선택속성의 조합으로 인해 관광지 만족도가 결정되는지 규명하고, 또 차후 연구 확장에도 기여했다.

3. 김경주. "정량적 텍스트 분석을 통한 품질성과 지표 연구." (2023)
  > - 주제 : TF-IDF & QFD
  > - 리뷰 : 단어 빈도 분석을 통해 품질요인 키워드의 TF-IDF 값을 도출하는 과정을 통해 핵심품질요인을 설정하는 과정을 알 수 있음. 이후 QFD로 도출된 값으로, QTI 모델의 실무 적용안으로서의 기업 품질경영 수준 및 차이점을 분석할 수 있음.

4. 서정태. 최승담 "QFD를 활용한 비교우위관점에서의 지역 관광경쟁력 결정요인 도출" (2007)
  > - 주제 : QFD & 지역 관광 평가 척도
  > - 리뷰 : 척도는 지역 내 관광자원에서 비롯되는 정성적인 고객요구(비교우위)를 QFD방법으로 전개시켜 도출된 정량적인 품질요소(경쟁우위)에 객관적인 가중치를 부여해 척도를 개발했다는 특징. 따라서 다양한 평가관점에 맞는 정량적인 측정단위이며, 제한된 질문 항목으로 효율적인 측정이 가능.

5. 장보위. "문화관광축제의 매력속성이 축제만족, 지역애착과 재방문의도에 미치는 영향." (2023)
  > - 주제 : 관광 축제 속성 파악
  > - 리뷰 : 매력속성 중 독특성’, ‘접근성’, ‘편의성’ 요인이 축제만족에 긍정적 영향을 미침. 축제만족은 지역애착과 재방문의도에, 지역애착은 재방문 의도에 영향을 미침.

기존연구의 한계점:
- 관광 축제의 속성에 대한 연구는 많지만 그 관광지의 매력을 결정하는 속성이 무엇인가에 집중한 연구가 대부분이다. 도출한 관광 속성을 이용해서 기존 관광지의 문제를 개선하거나 관광개발과 어떻게 연결지어 볼 수 있는지에 대한 연구는 많지 않다.
- 관광지에 대한 재방문, 만족도를 추가적으로 연구한 사례는 있으나 이는 연구방법에 있어 단순한 설문조사, 문헌조사 정도를 사용해 현재로서 **충분한 신뢰**를 갖는다고 판단하기 어렵다.
> LDA 토픽모델링의 결과를 FsQCA 분석으로 확장한 것을 참고하여, 토픽 모델링 도출 값을 QFD방법으로 전개시켜 정량적인 속성값(키워드)에 객관적인 가중치를 부여한다. 이를 통해 제한된 질문 항목으로 효율적인 측정이 가능함을 안다.

</br>

### 방법론:
1. KoBERTopic
> BERT embeddings과 클래스 기반(class-based) C-TF-IDF를 활용하여 문서의 중요한 단어를 유지하면서, 쉽게 해석할 수 있는 조밀한 클러스터를 만드는 토픽 모델링

<img width="498" alt="image" src="https://github.com/eunnnholee/Regional-Festival-Satisfaction-Improvement/assets/151797888/f2da304e-de51-47a7-8a7d-9671a75a7440">
</br>
해당 토픽모델을 선택한 이유:
1. 대규모 텍스트 데이터로 사전에 학습된 모델을 사용하여 적은 양의 데이터로 효과적인 결과 추출 가능 
2. 텍스트 데이터의 특성에 따라 토픽 수를 유연하게 조절할 수 있어 다양한 데이터에 대한 적응성이 우수 
3. BERT 모델의 특성상 단어의 의미를 파악할 때 문맥을 고려

</br>

### 설치 패키지: 
- python 3

```
pip install selenium
pip install chromedriver-autoinstaller
pip install konlpy
pip install bertopic
```

</br>
</br>

## II. 데이터 분석

### 전처리
- URL 및 e-mail 형태의 문자열 제거   
- 연속된 공백을 하나로 줄임
- 특수문자 제거
- 불용어 처리

</br>

### Topic Modeling
**각 토픽별 중요도 체크**
```
test_data = []

for i in range(19):
    topic_info = model.get_topic(i)
    test_data.append(topic_info)

    probabilities = [topic_info[1] for topic_info in topic_info]
    average_probability = sum(probabilities) / len(probabilities)

    print('{}번째 토픽의 평균 확률값(중요도): {:.4f}'.format(i+1, average_probability))
```
- KoBERTopic ▶ What List 구성
- 토픽 별 중요도 체크 ▶ What List의 중요도 확인
> **기존에는 설문조사를 통해 What List의 중요도를 확인하는데, 토픽 별 중요도를 비교함으로써 더 정량적인 방법을 선택**

<img width="93" alt="image" src="https://github.com/eunnnholee/Regional-Festival-Satisfaction-Improvement/assets/151797888/856bea51-6e3f-4e75-916a-31d17367a75f">

</br>

### QFD(Quality Function Deployment)
```
0 번째 토픽 : [('정책', 0.066823982673843), ('카페', 0.06479771811655109), ('가요', 0.032404426245441736), ('남편', 0.027060940459082455), ('내일', 0.0246815110424776), ('아기', 0.023564718738392238), ('주말', 0.022378024120492425), ('아이', 0.02235063759180107), ('가도', 0.019468795344531095), ('숙소', 0.01939273374524409)]
1 번째 토픽 : [('참여', 0.028596836445751415), ('체험', 0.027733733331780065), ('문화', 0.026881266249948667), ('프로그램', 0.024514911632640815), ('어린이', 0.02280345180375537), ('가족', 0.02205322148246891), ('이벤트', 0.019985428374189807), ('페스티벌', 0.019801189024081983), ('장소', 0.019364983525629577), ('카페', 0.01916263643310139)]
2 번째 토픽 : [('힐링', 0.10461471356488022), ('신청', 0.058127875462738586), ('조리', 0.053839225091425275), ('이미지', 0.05179457388646833), ('완료', 0.04517393730816833), ('이벤트', 0.044178610241235386), ('기간', 0.04218425897246597), ('할로윈', 0.04059841754970288), ('구경', 0.037927032740414944), ('결제', 0.031922628191370934)]
3 번째 토픽 : [('여름', 0.1132686992327061), ('한강', 0.0852490179177049), ('댕댕', 0.07951500558008995), ('머드', 0.06114438141968467), ('혠이바', 0.05505667366826157), ('세인트존스', 0.04931480476757452), ('인피니티', 0.04931480476757452), ('몽땅', 0.048932311126209195), ('생태', 0.043594699205983356), ('호캠카', 0.043398585397523066)]
4 번째 토픽 : [('딸기', 0.1528197853695685), ('빕스', 0.04986065624020194), ('장미', 0.03621404499358265), ('구경', 0.03561964922147837), ('메뉴', 0.033268458601396426), ('사진', 0.029681143818555678), ('체험', 0.02894087766913863), ('튤립', 0.02777642307629254), ('힐링', 0.027659886649666496), ('날씨', 0.025926208118028333)]
5 번째 토픽 : [('퀴어', 0.05757650581625565), ('동성애', 0.029565190368439753), ('반대', 0.028566065623076533), ('장소', 0.02560887129552859), ('봄꽃', 0.0231889349282664), ('나라', 0.022818299371860497), ('한국', 0.022645122004168534), ('기간', 0.022012513318359517), ('동성애자', 0.021819889250445212), ('문화', 0.02166792976511014)]
6 번째 토픽 : [('한우', 0.06047852539880024), ('횡성', 0.05526766894231643), ('고기', 0.043056856977982734), ('구매', 0.03936988332550727), ('체험', 0.03848924375547132), ('푸드', 0.03674492936423868), ('소고기', 0.031860091781870034), ('버섯', 0.028304101622039782), ('갈비', 0.028093525098310774), ('더덕', 0.02693612059983635)]
7 번째 토픽 : [('빙어', 0.090154135342784), ('겨울', 0.0886710353154051), ('얼음', 0.07303067911792135), ('눈꽃', 0.05590911228750642), ('불빛', 0.043284183205830676), ('썰매', 0.040673673186891655), ('낚시', 0.03825939369611878), ('상품권', 0.036654368756216), ('아이', 0.03362283067821953), ('산천어', 0.03302236498621226)]
8 번째 토픽 : [('유리', 0.08705553617910539), ('구경', 0.03644550802399248), ('시간', 0.032870805500085976), ('산후조리원', 0.03224693114096481), ('체험', 0.029748977985999705), ('제주도', 0.02599301927099795), ('방문', 0.02582073063366604), ('가을', 0.025572893871878156), ('아이', 0.02291956291231964), ('캠핑', 0.022283628280155433)]
9 번째 토픽 : [('어린이', 0.06524137063592565), ('아이', 0.05838001873892739), ('시민', 0.04404326540850155), ('구석기', 0.04098352027964784), ('어린이날', 0.04092336880092046), ('공원', 0.03790629961309901), ('온라인', 0.03715920437207533), ('참여', 0.035064180288422654), ('선비', 0.03345309637096353), ('공연', 0.03284662469670256)]
10 번째 토픽 : [('카페', 0.06915704624153461), ('공연', 0.06388517830918297), ('정책', 0.0634088891415483), ('예매', 0.0454015956595277), ('경의선', 0.04504105579220342), ('책거리', 0.04504105579220342), ('진실', 0.04132442353910864), ('관람', 0.040097364603883794), ('거짓', 0.03751568172391135), ('플로우', 0.03751568172391135)]
11 번째 토픽 : [('성인', 0.1277721514600786), ('만화', 0.12380393808431818), ('입장료', 0.08729624816492257), ('임산부', 0.0728585668045855), ('대요', 0.06799009643539032), ('입상', 0.06471794234047919), ('동상', 0.06471794234047919), ('연합뉴스', 0.06471794234047919), ('닭강정', 0.06471794234047919), ('회의', 0.06471794234047919)]
12 번째 토픽 : [('학부모', 0.054893500123568334), ('퀴어', 0.054203823467186274), ('아이', 0.049866831441030185), ('화가', 0.045191820832512046), ('친정', 0.04440370046194656), ('경찰', 0.044398023222333084), ('보험', 0.04120948892349645), ('동구청', 0.04013767234021557), ('남편', 0.037564288503378056), ('소원', 0.035326043189102756)]
13 번째 토픽 : [('애슐리', 0.09905858196651776), ('낚시', 0.06783854922707767), ('빙어', 0.06458756587002742), ('은어', 0.06243263109231433), ('연어', 0.04326474989967209), ('마리', 0.041218271963293286), ('퐁듀', 0.0408906649330929), ('썰매', 0.04006631101502573), ('코스', 0.04006631101502573), ('물고기', 0.03851416010608181)]
14 번째 토픽 : [('전등', 0.047384621705817837), ('뽀뽀', 0.04219634370259823), ('생일', 0.04219634370259823), ('놀이터', 0.03928165189477104), ('여행', 0.03675294907095039), ('사람', 0.03568775397033955), ('막둥이', 0.03553846627936338), ('남편', 0.03537245103160497), ('노라조', 0.03428504624058742), ('용기', 0.03326139237314854)]
15 번째 토픽 : [('사람', 0.09606854982924737), ('삼바', 0.08830770408811506), ('거리', 0.08083401361901975), ('고민', 0.0780959911911304), ('주말', 0.05574327097809817), ('하필', 0.05390991409561653), ('할로윈', 0.05238047578965162), ('사진', 0.04861704299489082), ('무리', 0.04710714377188074), ('토요일', 0.04671482083471772)]
16 번째 토픽 : [('노래', 0.1939766630340239), ('내빈', 0.08957808650114261), ('가수', 0.08621167248199456), ('무대', 0.07550217581982077), ('박지헌', 0.058246148106431264), ('동생', 0.05666166065962391), ('싸이', 0.05543270495348646), ('공연', 0.054615564201576025), ('성격', 0.05078596070811981), ('가요제', 0.048576454728814965)]
17 번째 토픽 : [('아기', 0.08961398911133263), ('카시트', 0.07595223475841618), ('산책', 0.05972856514951178), ('유모차', 0.05711934943776618), ('집앞', 0.051279876316576364), ('메밀', 0.04799759058107123), ('강아지', 0.04412111247458465), ('엄마', 0.03925923706878826), ('남편', 0.03919649979177847), ('처음', 0.03855770212089376)]
18 번째 토픽 : [('황소', 0.42953300101394865), ('흠뻑', 0.19705164533519035), ('변화', 0.18183014573366263), ('미나리', 0.16784068054839443), ('태풍', 0.15579115103965108), ('백종원', 0.15121655502439804), ('연기', 0.1437683927184487), ('동물', 0.1340561504354019), ('주의', 0.13289876586301644), ('영상', 0.11677680613218346)]
19 번째 토픽 : False
20 번째 토픽 : False
21 번째 토픽 : False
22 번째 토픽 : False
23 번째 토픽 : False
24 번째 토픽 : False
25 번째 토픽 : False
26 번째 토픽 : False
27 번째 토픽 : False
28 번째 토픽 : False
29 번째 토픽 : False
```




​
