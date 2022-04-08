# DA mini_Project (국민건강보험공단 > 검강검진 정보분석)

## ① 분석할 병 column 및 기준
**1. 비만**
> 참고할 기존 columns : 신장(5Cm단위), 체중(5Kg 단위)   
> BMI 계산     : 체중(kg)를 키(m)의 제곱으로 나눈 값

|   |저체중|정상|과체중|비만|
|---|---|---|---|---|
|BMI| BMI <= 18.5|18.5 < BMI <= 25| 25 < BMI <= 30 | 30 < BMI |


**2. 복부비만**
> 참고할 기존 columns : 허리둘레  

|   |해당|비해당|
|---|---|---|
|여성|85cm 이상|85cm 미만|
|남성|90cm 이상|90cm 미만|

**3. 혈압**
> 참고할 기존 columns : 수축기 혈압, 이완기 혈압

|   |저혈압|정상|고혈압
|---|---|---|---|
|이완기 혈압| v <= 60mmHg | 60mmHg < v < 95mmHg | 95mmHg <= v |
|수축기 혈압| v <= 100mmHg | 100mmHg < v < 145mmHg | 145mmHg <= v |
 
**4. 당뇨**
> 참고할 기존 columns : 식전혈당(공복혈당) 

|   |정상|질환 위험|질환 의심|
|---|---|---|---|
|공복 혈당| v <= 120mg/dL | 120mg/dL < v < 126mg/dL | 126mg/dL <= v |

**5. 간 기능 이상**
> 참고할 기존 columns : (혈청지오티)AST, (혈청지오티)ALT

|   |정상|질환 위험|질환 의심|
|---|---|---|---|
|AST| v <= 32U/L | 32U/L < v < 51U/L | 51U/L <= v |
|ALT| v <= 32U/L | 32U/L < v < 46U/L | 46U/L <= v |

**6. 빈혈**
> 참고할 기존 columns : 혈색소 

|   |해당|비해당|
|---|---|---|
|여성|12 이하|12 초과|
|남성|13 이하|13 초과|

----------------------------------------------------------------------------
## ② 결측치 처리

결측치가 있는 데이터 갯수가 총 갯수의 1% 미만을 차지 : dropna

----------------------------------------------------------------------------
## ③ 최종 DataFrame 
* df.head()   
![image](https://user-images.githubusercontent.com/37467592/162133692-8518cfbc-d1bc-4102-a8ea-4271db8cce71.png)

* df.info()   
![image](https://user-images.githubusercontent.com/37467592/162133833-ac5eaa3a-178e-44fd-ac12-cd05d77c6c17.png)

----------------------------------------------------------------------------
## ④ 데이터 분석

* 흡연상태
  + 비만
  ![image](https://user-images.githubusercontent.com/37467592/162372980-405e5157-ca52-4b29-b1f3-d6dc6a84b7d9.png)
  + 당뇨
  ![image](https://user-images.githubusercontent.com/37467592/162372912-78e3c020-a414-4ae0-9ef4-89beaa032f11.png)

  + 혈압
  ![image](https://user-images.githubusercontent.com/37467592/162373054-7796af1f-50c4-4340-8b8a-b71e60759093.png)

  + 간 기능 이상
  ![image](https://user-images.githubusercontent.com/37467592/162373110-f7d72d3a-ff60-41a5-90d6-c465ae3b8032.png)

  + 빈혈

* 음주 여부
  + 비만
  + 복부비만
  + 당뇨
  + 혈압
  + 간 기능 이상
  + 빈혈

* 성별
  + 비만
  + 복부비만
  + 당뇨
  + 혈압
  + 간 기능 이상
  + 빈혈

* 연령대별
  + 비만
  + 복부비만
  + 당뇨
  + 혈압
  + 간 기능 이상
  + 빈혈

* 지역별
  + 비만
  + 복부비만
  + 당뇨
  + 혈압
  + 간 기능 이상
  + 빈혈
