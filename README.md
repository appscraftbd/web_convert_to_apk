# web_convert_to_apk

manifests
```bash
<uses-permission  android:name="android.permission.INTERNET"></uses-permission>

```

xml code here
</br>layout:  RelativeLayout
```bash
  <WebView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:id="@+id/webview"
        />

```
import java
```bash
import android.webkit.WebSettings; 
import android.webkit.WebView; 
import android.webkit.WebViewClient;
```


varaible assign
```bash
private WebView mywebView;
```
java onecreate bundle

```bash
 mywebView = findViewById(R.id.webview);

 mywebView.setWebViewClient(new WebViewClient());

 mywebView.loadUrl("https://...................../");

 WebSettings webSettings=mywebView.getSettings();
 webSettings.setJavaScriptEnabled(true);
```



```bash
public class mywebClient extends WebViewClient{
        @Override
        public void onPageStarted(WebView view, String url, Bitmap favicon){
            super.onPageStarted(view,url,favicon);
        }
        @Override
        public boolean shouldOverrideUrlLoading(WebView view,String url){
            view.loadUrl(url);
            return true;
        }
    }
@Override
    public void onBackPressed(){
        if(mywebView.canGoBack()) {
            mywebView.goBack();
        }
    else{
        super.onBackPressed();
            }
}

```


