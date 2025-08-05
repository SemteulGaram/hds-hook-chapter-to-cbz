# Chapter CBZ Converter
Kurt Bestor의 Hitomi Downloader용 플러그인 Script(*.hds)

`extractor.manatoki_downloader.Downloader_manatoki` 프로필로 다운로드 된 만화 챕터를 rename Hook에서 챕터별로 CBZ 파일로 압축하는 스크립트입니다.

## 옵션
- 스크립트 상단에 있는 변수를 수정하고 적용하면 됩니다.
- `DELETE_ORIGIN`: 원본 폴더를 삭제할지 여부. `True`로 설정하면 원본 폴더가 삭제됩니다.
- `COPY_TO_PATH`: CBZ 파일을 복사할 경로. 빈 문자열이면 복사하지 않습니다. 예를 들어, `"D:\\Comics"`로 설정하면 `D:\Comics\[제목]\[챕터].cbz` 형태로 복사됩니다. 상대 경로 가능(ex. `"../OnlyCBZs"`).

## 삭제 방법
- 플러그인을 옵션에서 제거한뒤 `unhook.hds` 파일을 플러그인에 추가하면 Hook이 해제됩니다. 그 후 `unhook.hds` 플러그인도 제거하면 됩니다.

## 주의사항
- HD의 원본 압축 방법과는 호환되지 않습니다. 설정 > `Compression` > `Manatoki`를 `pass` 값으로 설정해야합니다.
- 원하는 다른 다운로드를 설정하고 싶으면 다운로더 문자열을 수정하세요.


바이브 환경 - Claude Code (Claude Sonnet 4)(20250805)
