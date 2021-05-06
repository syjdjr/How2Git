## 1. table extention 

- table이란 데이터를 행,열에 맞추어 배열하는 것이다. 


> #### [표현 방법] : | 사용하기 
>> 1. **행과 열에 맞게** 원하는 텍스트 데이터를 기입한다.  
>> 2. line 제일 **처음과 끝**, 그리고 **데이터들 사이**에 |를 넣어 cell을 구분시킨다.  
>> 3. 이때, table은 무조건 **-** *(hyphen)* 을 포함한 **delimiter row**가 있어야 한다. 
> - *주의점 : block 수준의 요소들은 table에 넣을 수 없다.* 
> - *주의점 : cell끼리 길이를 맞추지 않아도 된다.* 
>
|delimiter row 구성 방법|내용| 
|--| --| 
|방법1|hyphen ( - ) 사용하기|  
|방법2|colon ( : )  사용하기|  
|방법3|좌 , 우, 가운데,를 각각 할당하여 나타낸다.| 

![24865E76-3827-4067-8468-A15E176377EF](https://user-images.githubusercontent.com/81100851/112734565-f0e89d00-8f89-11eb-90e6-83aaacb69188.png)
![7129BD2B-44D2-492F-BEB0-EAB1951C0BDA](https://user-images.githubusercontent.com/81100851/112734568-f3e38d80-8f89-11eb-93c8-ed9d5b9ddc6a.png)


### 2. task list extention 
- task list는 추가적인 수행 단계를 list item들로 나타낼 수 있으며 이는 check box 형태로 표현 된다.  
> #### [표현 방법] : \- [] 사용하기 
>> 1. - 사용하여 task list 임을 알린다. 
>> 2. [] 을 사용하는데, 이때 [] 안에 space 혹은 글자 **x**를 넣어준다. 이는 checkbox 형태에서 unchecking 혹은 checking 형태로 나타날 것이다.
>> 3. [] 뒤에 기입하고자 하는 내용을 넣는다. 
>> 4. 들여쓰기하여 새로운 task list를 만들 수 있다. 

![EA86B94E-A199-46F4-A713-BBFB1EB2EC46](https://user-images.githubusercontent.com/81100851/112734581-04940380-8f8a-11eb-8cb4-ad17ee1fa729.png)
![A14D8C31-19C1-480A-9210-25647234C3CA](https://user-images.githubusercontent.com/81100851/112734582-08278a80-8f8a-11eb-890f-15f2a3cc7247.png)

### 3. strike through extention
- 추가적인 강조를 할 수 있다.
> #### [표현 방법] : ~~ 사용하기 
>> 1. 원하는 단어나 구절 앞과 뒤에 **두개의 tildes ( ~~ )** 를 붙여준다. 

![E5C288E6-C86D-47A6-BEDC-2EA773AEA983](https://user-images.githubusercontent.com/81100851/112734697-baf7e880-8f8a-11eb-9ef8-0b919e11f116.png)
![88C4D2A1-829B-4D33-898D-E95B73AC4C41](https://user-images.githubusercontent.com/81100851/112734702-bdf2d900-8f8a-11eb-968d-77ddf1f900c5.png)

### 4. Autolinks extention
- 기존 링크를 더 단순하게 나타내고 hyperlink 해준다. 

|유형|특징|
|--|--|
|www로 시작하는 주소| 1. www. 은 autolink로 자동 인식 된다.<br> 2. paragraph 내에서 autolink를 활용할 수 있다. |
|\)로 끝나는 주소|1. 삽입 어구의 total number를 이용하여 인지한다.<br> 2. autolink 안에 있는 삽입어구는 신경쓰지 않는다. |
|;로 끝나는 주소|1. &를 이용하여 뒤에 1개 이상의 알파벳 character가 있는 경우 entity reference와 비슷한지 확인해야 한다.<br> 2. entity reference는 autolink에서 제외 된다.| 
|URL|  http:// 혹은 https:// 중 하나일때 URL이 인식된다.|
|email|1. text node 1개 이상 있을 때 인지된다.<br> 2. **alphanumeric과 -와_ 는 한개 이상의 .을 가지고 있어야 인지된다** <br> *단, 이때, text node 중  ~~- 와 _ 는 맨 끝의 character~~가 되서는 안된다.*<br> *또한, Trailing punctiation( . ? ! , : * _ ~) 은 autolink로 고려되지 않는다.*|

> *text node란 alphanumeric 혹은 . - _ + @ 을 나타낸다.* <br>

> *주의 : Autolinks 나타내는 link들은 모두 space 와 -< character가 없어야 한다.* 


### 5. Disallowed Raw HTML extention
- HTML 산출물을 선별할때 HTML tags를 고르는 tagfilter extention이 
가능하다. 
> [표현 방법] : 
>> Filtering은 \<로 시작되거나 &lt\;로 시작되어야 한다. 

>- \<title\>
>- \<textarea\>
>- \<style\>
>- \<xmp\>
>- \<iframe\>
>- \<noembed\>
>- \<noframes\>
>- \<script\>
>- \<plaintext\>

![3C20FD71-49B7-48F6-AEE0-DBBE01D21C0E](https://user-images.githubusercontent.com/81100851/112743003-8dcd2980-8fce-11eb-87a1-6833d7e58b40.jpeg)
![311DA8FF-E071-4979-9619-E438D0BFA433](https://user-images.githubusercontent.com/81100851/112743004-90c81a00-8fce-11eb-9e8d-6fbd8123d95b.jpeg)
