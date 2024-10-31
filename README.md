## Note
This Go project implements Tencent-RTC's UserSig authentication, providing a secure server-side method for generating signatures to protect the keys from leakage.

![](https://cloudcache.intl.tencent-cloud.com/cms/backend-cms/12569f72920411ef810152540055f650.png)

## Usage
``` go
import (
	"github.com/tencentcloud/tls-sig-api-v2-golang/tencentcloud"
	"fmt"
)

const (
	sdkappid = 1400000000
	key = "5bd2850fff3ecb11d7c805251c51ee463a25727bddc2385f3fa8bfee1bb93b5e"
)

func main()  {
	sig, err := tencentcloud.GenSig(sdkappid, key, "xiaojun", 86400*180)
	if err != nil {
		fmt.Println(err.Error())
	} else {
		fmt.Println(sig)
	}
}
```
