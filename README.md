
# php-namumark-mediawiki (No External)
php-namumark-mediawiki (No External)는 [나무위키](https://namu.wiki)에서 사용하는 [나무마크](https://namu.wiki/w/%EB%82%98%EB%AC%B4%EC%9C%84%ED%82%A4:%ED%8E%B8%EC%A7%91%20%EB%8F%84%EC%9B%80%EB%A7%90)를 미디어위키 확장기능으로 구현한 것에서 외부 이미지/동영상을 이용하는 코드를 삭제한 것입니다. 오리위키 운영자 김동동이 만든 원본은 [이곳](https://github.com/Oriwiki/php-namumark-mediawiki/archive/master.zip)을 참조하세요.

[php-namumark 라이브러리](https://github.com/koreapyj/php-namumark)를 바탕으로 구성되어 있습니다.

수정 - 밑줄 매직워드 추가, 각주 문법 추가(소괄호 2), 글자 확대 효과 추가 (9단계), 중괄호 3개로 nowiki효과 제거, $$표시로 수식 삽입 가능, {{{#!html 문법 비활성화.

## 라이선스
본 확장기능은 GNU Affero GPL 3.0에 따라 자유롭게 사용하실 수 있습니다. 라이선스에 대한 자세한 사항은 첨부 문서를 참고하십시오.

## 의존
* [Cite 확장기능](https://www.mediawiki.org/wiki/Extension:Cite)
* [Math 확장기능](https://www.mediawiki.org/wiki/Extension:Math) 또는 [SimpleMathJax 확장기능](https://www.mediawiki.org/wiki/Extension:SimpleMathJax)
* [Poem 확장기능](https://www.mediawiki.org/wiki/Extension:Poem)
* [SyntaxHighlight 확장기능](https://www.mediawiki.org/wiki/Extension:SyntaxHighlight)

## 사용 방법
1. 미디어위키 extensions 폴더에 NamuMark 폴더를 새로 생성합니다. 또는 서버에 직접 git을 이용하실 수 있으면 설치된 미디어위키의 extensions 폴더에서 다음과 같이 명령합니다.

		git clone https://github.com/Oriwiki/php-namumark-mediawiki.git NamuMark

1. [여기](https://github.com/Oriwiki/php-namumark-mediawiki/archive/master.zip)를 눌러 다운받은 다음 압축을 풀고, 압축이 풀린 파일을 모두 NamuMark 폴더에 넣습니다. (git으로 한 경우 필요 없습니다.)
1. LocalSettings.php에 다음을 입력합니다.

    ```php
    require_once "$IP/extensions/NamuMark/namumark.php";
    $wgRawHtml = true;
    $wgAllowImageTag = true;
    ```

	
## 그 외
이 코드는 나무마크의 기능 중에서 보안상의 문제를 야기할 수 있는 외부 이미지 혹은 동영상을 불러들일 수 있는 기능을 제거하였습니다. 원본에서 추가한 기능은 없으니 제거할 이유가 없다면 [원본](https://github.com/Oriwiki/php-namumark-mediawiki/archive/master.zip)을 참조하세요.

자세한 사항에 대해서는 [오리위키의 설명 페이지](http://oriwiki.net/%EB%8F%84%EC%9B%80%EB%A7%90:%EC%9C%84%ED%82%A4_%EB%AC%B8%EB%B2%95/%EB%82%98%EB%AC%B4%EB%A7%88%ED%81%AC)를 참고해주시길 바랍니다.

아직까지 라이브러리의 기능이 완벽하게 구현돼있지 않습니다. 이점을 참고하시고 실제 미디어위키 사이트에 적용하실 때에는 반드시 사전에 시험해보실 것을 권장하는 바입니다.

