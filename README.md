# Chapter CBZ Converter
Kurt Bestor의 Hitomi Downloader용 플러그인 Script(*.hds)

`extractor.manatoki_downloader.Downloader_manatoki` 프로필로 다운로드 된 만화 챕터를 rename Hook에서 챕터별로 CBZ 파일로 압축하는 스크립트입니다.

## 왜?
- 원 프로그램에 zip, cbz 압축 기능이 있지만, [챕터별로 압축하는 기능을 만들고 싶어하지 않는 것 같습니다...](https://github.com/KurtBestor/Hitomi-Downloader/issues/154)
- 원본 파일을 그대로 다른 기기로 동기화 하거나 하면 파일이 너무 많아져서 불편하고, 압축하면 모든 책이 하나의 압축파일이 되어서 챕터를 찾기 불가능해져서 만들었습니다.

## 옵션
- 스크립트 상단에 있는 변수를 수정하고 적용하면 됩니다.
- `DELETE_ORIGIN`: 원본 폴더를 삭제할지 여부. `True`로 설정하면 원본 폴더가 삭제됩니다.
  - > 주: 기본값인 `False`로 두는게 낫습니다. 원본 폴더를 삭제하면 나중에 다시 다운로드할 때 전체 챕터를 계속 다시 받아서 오래걸립니다...
- `COPY_TO_PATH`: CBZ 파일을 복사할 경로. 빈 문자열이면 복사하지 않습니다. 예를 들어, `"D:\\Comics"`로 설정하면 `D:\Comics\[제목]\[챕터].cbz` 형태로 복사됩니다. 상대 경로 가능(ex. `"../OnlyCBZs"`).
  - > 주: 이전 옵션에서 `False`를 선택한 경우 다른 장치에 동기화해서 볼 예정이라던지라면 이 옵션을 사용하는게 좋습니다...

## 설치 방법
- `hook_chapter_to_cbz.hds` 파일을 텍스트 에디터로 열어 옵션을 수정한뒤, 프로그램 설정의 plugin에 추가합니다.

## 삭제 방법
- 플러그인을 옵션에서 제거한뒤 `unhook.hds` 파일을 플러그인에 추가하면 Hook이 해제됩니다. 그 후 `unhook.hds` 플러그인도 제거하면 됩니다.

## 주의사항
- HD의 원본 압축 방법과는 호환되지 않습니다. 설정 > `Compression` > `Manatoki`를 `pass` 값으로 설정해야합니다.
- 원하는 다른 다운로드를 설정하고 싶으면 다운로더 문자열을 수정하세요.


바이브 환경 - Claude Code (Claude Sonnet 4)(20250805)
