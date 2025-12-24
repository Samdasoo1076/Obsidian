```
- onLoad()                                                                    Froala 에디터 생성/초기화. 업로드 URL, 툴바, 언어 설정 후 Editor_Complete() 호출. 
  - Editor_Complete()                 
    부모(또는 parent.parent) 쪽의 Editor_Complete() 호출해 에디터 준비 완료 통지 
  - setEditMode(modenum)
    "1"이면 편집 가능, 아니면 편집 비활성화.
  - SetEditorContent(Data) / SetEditorContent2(Data)
    에디터 HTML 내용을 설정(예외 처리 포함).        
  - GetEditorContent()      
    에디터 HTML 가져오기.      
  - GetContentView()           
    에디터 HTML 가져오기(= GetEditorContent와 유사).
  - GetBodyValue() / GetHtmlValue()
    에디터 HTML 반환(editor.html.get(true)).
  - GetTextValue() / GetEditorTextContent()
    에디터 HTML 텍스트 반환(실제는 html.get(false)라 HTML 그대로)                
  - Set_InsertHTML(pHTML)   
    현재 HTML 뒤에 문자열 추가해서 다시 세팅.  
  - GetFieldsList_Content()      
    에디터 HTML을 DIV에 넣고 전체 태그 목록 반환. 
  - GetValue(field) / SetValue(field, value)           
    에디터 HTML에서 특정 id 요소의 innerHTML 읽기/쓰기.
  - GetEditorContent_mediaChange(_media)                  
    에디터 HTML 내 video/audio source 경로를 _media 매핑으로 치환.              
  - SetEditorContentURL(pURL) / SetEditorContentURL_Path(pURL)
    MHT 변환 HTML을 불러와 에디터 내용으로 설정.     
  - SetEditorContentURL_Admin(pURL)
    MHT 변환 후 CONNINFO 분리, 본문만 세팅 + 연결정보 반환.  
  - GetEditorContentURL_Path(url)
    MHT 변환 HTML을 문자열로 반환.                 
  - GetImage() 
    에디터 HTML에서 <img> 태그 목록 반환.
```