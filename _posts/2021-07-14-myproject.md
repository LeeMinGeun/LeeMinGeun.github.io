---
layout: single
title: "나의 프로젝트"
---


개발자이름: 이민근
■ 개발 소프트웨어 이름 : 디데이 계산기

⊙ 요구사항
-문제분석: 개발할 프로그램의 기능과 제약조건, 목표 등을 명확히 정의 → 요구명세서 작성
-시스템 명세: 무엇을 수행하는가를 정의/입력자료, 처리내용, 출력이 무엇인지 정의 → 시스템 기능 명세서 작성

[문제 상황]
 동탄 중앙고 2학년 5반 이민근 학생은 학교 중간고사와 모의고사 스케줄에 맞춰 공부 계획을 세우려고 한다. 
 그러나, 중간고사와 모의고사까지 정확히 며칠이 남았는지 몰라 공부 계획을 세우는데 어려움을 겪고 있다고 한다. 
 이제 이 문제를 해결하여 이민근 학생이 중간고사와 모의고사까지 며칠 남았는지 쉽게 알 수 있도록 해야한다.


⊙ 설계
-프로그램 설계: 프로그램 내의 처리 절차나 알고리즘 설계
-사용자 인터페이스 설계: 사용자가 시스템을 사용하기 위해 보여지는 부분 설계

1. datetime 모듈을 이용합니다.
2. 중간고사 혹은 모의고사가 몇 월, 며칠인지 각각 입력받도록 합니다.
3. 입력받은 날짜와 오늘 날짜를 일수로 변환하고 정수 취급하여 차를 구합니다.
4. 차가 0보다 크면 며칠 남았는지 알려주고, 차가 0이면 당일이라고 알려주는 등 상황에 맞게 출력되도록 합니다.






⊙ 구현
-프로그래밍 언어를 사용하여 실제 프로그램을 작성하는 단계

~~~
import datetime
 
x = int(input('D-Day 구할 날 선택(중간고사:0,모의고사:1)'))
 
 
if x == 0:
 a1 = int(input('중간고사는 몇 월 입니까?')) #중간고사(10월 14일)
 a2 = int(input('중간고사는 며칠입니까?'))
 
 dt1 = datetime.datetime.now() 
 dt2 = datetime.datetime(2021, a1, a2) 
 a=int((dt2-dt1).days)
 
 if a > 0:
   print('중간고사까지 {}일 남았습니다.'.format(a))
 elif a == 0:
   print('오늘이 중간고사입니다!!!')
 else:
   print('중간고사가 끝났습니다.')
 
 
if x == 1:
  b1 = int(input('모의고사는 몇 월 입니까?')) #11월 모의고사(11월 24일)
  b2 = int(input('모의고사는 며칠입니까?'))
 
  dt1 = datetime.datetime.now() 
  dt3 = datetime.datetime(2021, b1, b2) 
  b=int((dt3-dt1).days)
 
  if b > 0:
   print('모의고사까지 {}일 남았습니다.'.format(b))
  elif b == 0:
   print('오늘이 모의고사입니다!!!')
  else:
   print('모의고사가 끝났습니다.')

~~~


⊙ 테스트
개발한 시스템이 요구사항을 만족하는지, 실행결과가 예상한 결과와 정확하게 맞는지를 검사하고 평가

D-Day 구할 날 선택(중간고사:0,모의고사:1)0
중간고사는 몇 월 입니까?10
중간고사는 며칠입니까?14
중간고사까지 57일 남았습니다.


D-Day 구할 날 선택(중간고사:0,모의고사:1)1
모의고사는 몇 월 입니까?11
모의고사는 며칠입니까?24
모의고사까지 98일 남았습니다.


⊙ 느낀점

  제가 평소에 필요하다고 느끼는 것을 직접 만들어보니까 굉장히 신기하면서도 보람찬 경험이었던 것 같습니다.
 특히, 제가 설계한 코드가 오류없이 잘 작동되었을 때의 짜릿함은 말로 설명할 수 없을 정도로 컸습니다.
 그뿐만 아니라 발표 활동을 통해 다른 친구들의 코드를 보면서 많은 것들을 배우고 얻어갈 수 있었던 것 같습니다. 
 2학기에도 기회가 된다면 저의 한계를 넘어선 개발을 한 번 해보고 싶다는 생각이 들었습니다. 
