# OlibFileuploadConfig
| Name | Type | Description |
|---|---|---|
|url|string|파일 업로드 서버 경로|
|accept|string|업로드 허용할 확장자(ex: .jpg .png)|
|maxFileSize|string|최대 업로드 파일 허용 크기(bytes)|
|credentials|string|인증 토큰 사용 여부('true':사용, 'false' : 미사용|
|authToken|string|인증토큰 (credentials 값이 true 일경우 필수)|

---
# OlibFileupload
| Name | Type | Description |
|---|---|---|
|idx|number|업로드 파일 인덱스|
|fileSize|number|업로드 파일 크기|
|viewFileName|string|표시할 파일명|
|realFileName|string|저장된 실제 파일명|
|filePath|string|저장된 파일 경로|