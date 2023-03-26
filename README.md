# WebViewControlInfo

android 웹 뷰를 컨트롤하는 방법을 모아 놓은 Repository입니다.



## 파일 업로드

웹 뷰에서 파일을 업로드 하기 위해선 webChromeClient를 새로 할당해야합니다.

그러기 위해선 먼저 WebChromeClient를 상속 받은 새 클래스를 생성합니다.

```kotlin
class CustomWebChromeClient : WebChromeClient() {

    override fun onShowFileChooser(
        webView: WebView?,
        filePathCallback: ValueCallback<Array<Uri>>?,
        fileChooserParams: FileChooserParams?
    ): Boolean {
            super.onShowFileChooser(webView, filePathCallback, fileChooserParams)

    }
}

```

WebChromeClient에는 onShowFileChooser 함수가 있습니다.

이를 override하여 파일 업로드를 처리할 수 있습니다.

return value를 false
