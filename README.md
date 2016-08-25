# WebViewTest

第一行代码中该demo无法使用，从写了一下，供参考学习。

之前的 shouldOverrideUrlLoading(WebView view, String url)该方法已经被弃用，所以原demo无法使用了。

推荐使用shouldOverrideUrlLoading(WebView view, WebResourceRequest request)这个方法，看代码吧

#  注意 

 添加网络的权限 
#  重点 
---

mWebView.setWebViewClient(new WebViewClient(){

            @Override
            public boolean shouldOverrideUrlLoading(WebView view, WebResourceRequest request) {
                //重中之重
                view.loadUrl(request.toString());
                Log.d(TAG, "shouldOverrideUrlLoading: "+request.toString());
                return true;
            }
        }
        
--- 
