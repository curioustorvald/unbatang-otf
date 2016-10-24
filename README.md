__은바탕OTF__는 은광희 님의 한글 LaTeX 포스트스크립트 Type1 글꼴을 otf로 담고, 몇몇 글리프를 수정하고, 2개 웨이트(굵기)를 추가한 글꼴 묶음입니다.

원 글꼴의 힌팅 정보가 그대로 보존되어 있으므로 LaTeX을 이용하여 PDF 문서를 작성했을 때 작은 글꼴 크기에서 윈도 운영체제에서도 양호하게 보입니다. (다만 이 힌팅 정보는 컴퓨터 화면을 위한 것이 아닙니다)


## 수정 사항 ##

* 물음표와 느낌표의 모양을 평범한 모양으로 바꾸었습니다.
* 「, 『, 」, 』, 〈, 《, 〉, 》 괄호의 높이를 알맞게 조정하였습니다.
* 2개 웨이트(300, 450)를 추가하였습니다.


## 유의 사항 ##

* 원본이 HLaTeX에서 직접 추출한 글꼴이라 옛한글 구현을 위한 GSUB정보는 없습니다.
* LaTeX 외에서 사용할 시 자간 등을 직접 손봐야 할 수 있습니다.
* LuaTeX-ko에서 세로쓰기가 작동하지 않습니다. (XeTeX-ko에서도 안 될 겁니다)


## LaTeX에서 사용하기 ##

luatexko 패키지를 사용 중일 때 다음과 같이 사용할 수 있습니다.

    \setmainfont{LinLibertineO}
    \setmainhangulfont{UnBatangOTF-Book}[BoldFont=UnBatangOTF-Bold, InterHangul=-.0852em, Protrusion, Expansion]\hangulpunctuations=1
    \registerpunctuations{"20, "2C, "2E, "3A, "3B, "3F, "2014, "2018, "2019, "201C, "201D}

가는체는 다음과 같이 추가하고 사용할 수 있습니다.

    \newfontfamily\hanlight{UnBatangOTF-Light}[InterHangul=-.0852em, Protrusion, Expansion]
    
    ...
    
    {\hanlight
    이 부분은 조판할 때 가는 글꼴로 표현됩니다.
    
    컴퓨터 출판물의 양이 늘면 타입킷의 활용도 많아지게 된다.
    }

