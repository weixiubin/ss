### surge配置shandowsocks(ss)
```
[General]
skip-proxy = 127.0.0.1, 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, localhost, *.local
bypass-tun = 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12
loglevel = notify
interface = 127.0.0.1
port = 1235
socks-port = 1234
dns-server = system, 114.114.114.114
enhanced-mode-by-rule = true

[Proxy]
随便起个名字 = custom,ip,port,AES-256-CFB,password,https://github.com/weixiubin/ss/blob/master/SSEncrypt.module

[Proxy Group]
Proxy = select,随便起个名字
Apple = select,DIRECT,Proxy

[Rule]
# Apple
DOMAIN-SUFFIX,s.mzstatic.com,Proxy
DOMAIN-SUFFIX,lcdn-registration.apple.com,DIRECT
DOMAIN-SUFFIX,ls.apple.com,DIRECT
DOMAIN-SUFFIX,mzstatic.com,DIRECT
DOMAIN,radio-activity.itunes.apple.com,Proxy
DOMAIN,radio.itunes.apple.com,Proxy
DOMAIN,radio-services.itunes.apple.com,Proxy
DOMAIN,init.itunes.apple.com,Proxy
DOMAIN,itunes.apple.com,Proxy
DOMAIN,client-api.itunes.apple.com,Proxy
DOMAIN,upp.itunes.apple.com,Proxy
DOMAIN,play.itunes.apple.com,Proxy
DOMAIN-SUFFIX,search.itunes.apple.com,Proxy
DOMAIN-KEYWORD,buy.itunes.apple.com,Proxy
DOMAIN,swscan.apple.com,Proxy
DOMAIN,su.itunes.apple.com,Proxy
DOMAIN,se.itunes.apple.com,Proxy
DOMAIN-SUFFIX,itunesconnect.apple.com,Proxy
DOMAIN-SUFFIX,lookup-api.apple.com,Proxy,enhanced-mode // Dictionary
DOMAIN-SUFFIX,apple.com,Apple
DOMAIN-SUFFIX,icloud.com,Apple
DOMAIN-SUFFIX,icloud-content.com,Apple
DOMAIN-SUFFIX,me.com,Apple
DOMAIN-SUFFIX,cdn-apple.com,Apple

# DNS polution
DOMAIN-SUFFIX,facebook.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,fb.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,fb.me,Proxy,force-remote-dns
DOMAIN-SUFFIX,fbcdn.net,Proxy,force-remote-dns
DOMAIN-SUFFIX,cdninstagram.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,instagram.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,scdn.co,Proxy,force-remote-dns
DOMAIN-SUFFIX,line.naver.jp,Proxy,force-remote-dns
DOMAIN-SUFFIX,t.co,Proxy,force-remote-dns
DOMAIN-SUFFIX,twimg.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,twitter.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,youtube-nocookie.com,Proxy
DOMAIN-SUFFIX,youtube.com,Proxy,force-remote-dns
DOMAIN,accounts.google.com,Proxy,force-remote-dns,enhanced-mode
DOMAIN-SUFFIX,appspot.com,Proxy,force-remote-dns
DOMAIN-SUFFIX,googleapis.com,Proxy,force-remote-dns,enhanced-mode
DOMAIN-SUFFIX,google.com,Proxy,force-remote-dns,enhanced-mode
DOMAIN-SUFFIX,gmail.com,Proxy,force-remote-dns
DOMAIN-KEYWORD,google,Proxy,force-remote-dns

# Accelerate top cn sites
DOMAIN-KEYWORD,alipay,DIRECT
DOMAIN-KEYWORD,baidu,DIRECT
DOMAIN-KEYWORD,taobao,DIRECT

DOMAIN-SUFFIX,cn,DIRECT
DOMAIN-SUFFIX,126.net,DIRECT
DOMAIN-SUFFIX,163.com,DIRECT
DOMAIN-SUFFIX,alicdn.com,DIRECT
DOMAIN-SUFFIX,amap.com,DIRECT
DOMAIN-SUFFIX,bdimg.com,DIRECT
DOMAIN-SUFFIX,bdstatic.com,DIRECT
DOMAIN-SUFFIX,ccgslb.com.cn,DIRECT
DOMAIN-SUFFIX,cnbeta.com,DIRECT
DOMAIN-SUFFIX,cnzz.com,DIRECT
DOMAIN-SUFFIX,douban.com,DIRECT
DOMAIN-SUFFIX,gtimg.com,DIRECT
DOMAIN-SUFFIX,hao123.com,DIRECT
DOMAIN-SUFFIX,haosou.com,DIRECT
DOMAIN-SUFFIX,ifeng.com,DIRECT
DOMAIN-SUFFIX,iqiyi.com,DIRECT
DOMAIN-SUFFIX,jd.com,DIRECT
DOMAIN-SUFFIX,netease.com,DIRECT
DOMAIN-SUFFIX,ourdvs.com,DIRECT
DOMAIN-SUFFIX,qhimg.com,DIRECT
DOMAIN-SUFFIX,qq.com,DIRECT
DOMAIN-SUFFIX,sogou.com,DIRECT
DOMAIN-SUFFIX,sohu.com,DIRECT
DOMAIN-SUFFIX,soso.com,DIRECT
DOMAIN-SUFFIX,steamstatic.com,DIRECT
DOMAIN-SUFFIX,steamcommunity.com,DIRECT
DOMAIN-SUFFIX,suning.com,DIRECT
DOMAIN-SUFFIX,tmall.com,DIRECT
DOMAIN-SUFFIX,tudou.com,DIRECT
DOMAIN-SUFFIX,weibo.com,DIRECT
DOMAIN-SUFFIX,youku.com,DIRECT
DOMAIN-SUFFIX,xunlei.com,DIRECT
DOMAIN-SUFFIX,zhihu.com,DIRECT
DOMAIN-SUFFIX,blackssl.com,DIRECT
DOMAIN-SUFFIX,darkssl.com,DIRECT
DOMAIN-SUFFIX,polarynetwork.com,DIRECT

# Top blocked sites
DOMAIN-SUFFIX,4sqi.net,Proxy
DOMAIN-SUFFIX,abpchina.org,Proxy
DOMAIN-SUFFIX,adblockplus.org,Proxy
DOMAIN-SUFFIX,akamaihd.net,Proxy
DOMAIN-SUFFIX,amazon.com,Proxy
DOMAIN-SUFFIX,amazonaws.com,Proxy,enhanced-mode
DOMAIN-SUFFIX,amplitude.com,Proxy
DOMAIN-SUFFIX,ampproject.com,Proxy
DOMAIN-SUFFIX,ampproject.net,Proxy
DOMAIN-SUFFIX,ampproject.org,Proxy
DOMAIN-SUFFIX,android.com,Proxy
DOMAIN-SUFFIX,angularjs.org,Proxy
DOMAIN-SUFFIX,aolcdn.com,Proxy
DOMAIN-SUFFIX,apple-dns.net,Proxy
DOMAIN-SUFFIX,appsto.re,Proxy
DOMAIN-SUFFIX,arcgis.com,Proxy
DOMAIN-SUFFIX,archive.org,Proxy
DOMAIN-SUFFIX,aspnetcdn.com,Proxy
DOMAIN-SUFFIX,att.com,Proxy
DOMAIN-SUFFIX,awsstatic.com,Proxy
DOMAIN-SUFFIX,azureedge.net,Proxy
DOMAIN-SUFFIX,azurewebsites.net,Proxy
DOMAIN-SUFFIX,bintray.com,Proxy,enhanced-mode
DOMAIN-SUFFIX,bit.com,Proxy
DOMAIN-SUFFIX,bit.ly,Proxy
DOMAIN-SUFFIX,bitbucket.org,Proxy
DOMAIN-SUFFIX,blog.com,Proxy
DOMAIN-SUFFIX,blogcdn.com,Proxy
DOMAIN-SUFFIX,blogger.com,Proxy
DOMAIN-SUFFIX,blogsmithmedia.com,Proxy
DOMAIN-SUFFIX,blogspot.com,Proxy
DOMAIN-SUFFIX,blogspot.hk,Proxy
DOMAIN-SUFFIX,bloomberg.com,Proxy
DOMAIN-SUFFIX,box.net,Proxy
DOMAIN-SUFFIX,cachefly.net,Proxy
DOMAIN-SUFFIX,chromium.org,Proxy
DOMAIN-SUFFIX,cl.ly,Proxy
DOMAIN-SUFFIX,cloudflare.com,Proxy
DOMAIN-SUFFIX,cloudfront.net,Proxy
DOMAIN-SUFFIX,cloudmagic.com,Proxy
DOMAIN-SUFFIX,cocoapods.org,Proxy
DOMAIN-SUFFIX,crashlytics.com,Proxy
DOMAIN-SUFFIX,d.pr,Proxy
DOMAIN-SUFFIX,dayone.me,Proxy
DOMAIN-SUFFIX,digicert.com,Proxy
DOMAIN-SUFFIX,disq.us,Proxy
DOMAIN-SUFFIX,disqus.com,Proxy
DOMAIN-SUFFIX,disquscdn.com,Proxy
DOMAIN-SUFFIX,dnsimple.com,Proxy
DOMAIN-SUFFIX,docker.com,Proxy
DOMAIN-SUFFIX,dribbble.com,Proxy
DOMAIN-SUFFIX,dropbox.com,Proxy
DOMAIN-SUFFIX,dropboxstatic.com,Proxy
DOMAIN-SUFFIX,dropboxusercontent.com,Proxy
DOMAIN-SUFFIX,droplr.com,Proxy
DOMAIN-SUFFIX,duckduckgo.com,Proxy
DOMAIN-SUFFIX,edgecastcdn.net,Proxy
DOMAIN-SUFFIX,edgesuite.net,Proxy
DOMAIN-SUFFIX,engadget.com,Proxy
DOMAIN-SUFFIX,eurekavpt.com,Proxy
DOMAIN-SUFFIX,evernote.com,Proxy
DOMAIN-SUFFIX,fabric.io,Proxy
DOMAIN-SUFFIX,fastly.net,Proxy
DOMAIN-SUFFIX,fc2.com,Proxy
DOMAIN-SUFFIX,feedburner.com,Proxy
DOMAIN-SUFFIX,feedly.com,Proxy
DOMAIN-SUFFIX,feedsportal.com,Proxy
DOMAIN-SUFFIX,flickr.com,Proxy
DOMAIN-SUFFIX,g.co,Proxy
DOMAIN-SUFFIX,ggpht.com,Proxy
DOMAIN-SUFFIX,git.io,Proxy
DOMAIN-SUFFIX,github.com,Proxy,enhanced-mode
DOMAIN-SUFFIX,github.io,Proxy
DOMAIN-SUFFIX,githubapp.com,Proxy
DOMAIN-SUFFIX,githubusercontent.com,Proxy,enhanced-mode
DOMAIN-SUFFIX,globalsign.com,Proxy
DOMAIN-SUFFIX,godaddy.com,Proxy
DOMAIN-SUFFIX,golang.org,Proxy
DOMAIN-SUFFIX,goo.gl,Proxy
DOMAIN-SUFFIX,goodreaders.com,Proxy
DOMAIN-SUFFIX,goodreads.com,Proxy
DOMAIN-SUFFIX,gravatar.com,Proxy
DOMAIN-SUFFIX,gstatic.com,Proxy
DOMAIN-SUFFIX,hotmail.com,Proxy
DOMAIN-SUFFIX,ift.tt,Proxy
DOMAIN-SUFFIX,ifttt.com,Proxy
DOMAIN-SUFFIX,imageshack.us,Proxy
DOMAIN-SUFFIX,img.ly,Proxy
DOMAIN-SUFFIX,imgur.com,Proxy
DOMAIN-SUFFIX,instapaper.com,Proxy
DOMAIN-SUFFIX,ipn.li,Proxy
DOMAIN-SUFFIX,is.gd,Proxy
DOMAIN-SUFFIX,itun.es,Proxy
DOMAIN-SUFFIX,j.mp,Proxy
DOMAIN-SUFFIX,jshint.com,Proxy
DOMAIN-SUFFIX,kat.cr,Proxy
DOMAIN-SUFFIX,libsyn.com,Proxy
DOMAIN-SUFFIX,licdn.com,Proxy
DOMAIN-SUFFIX,line.me,Proxy
DOMAIN-SUFFIX,line-apps.com,Proxy
DOMAIN-SUFFIX,line-scdn.net,Proxy
DOMAIN-SUFFIX,linkedin.com,Proxy
DOMAIN-SUFFIX,linode.com,Proxy
DOMAIN-SUFFIX,lithium.com,Proxy
DOMAIN-SUFFIX,live.com,Proxy
DOMAIN-SUFFIX,live.net,Proxy
DOMAIN-SUFFIX,mathjax.org,Proxy
DOMAIN-SUFFIX,medium.com,Proxy
DOMAIN-SUFFIX,mega.co.nz,Proxy
DOMAIN-SUFFIX,mega.nz,Proxy
DOMAIN-SUFFIX,megaupload.com,Proxy
DOMAIN-SUFFIX,mobile01.com,Proxy
DOMAIN-SUFFIX,modmyi.com,Proxy
DOMAIN-SUFFIX,name.com,Proxy
DOMAIN-SUFFIX,nextmedia.com,Proxy
DOMAIN-SUFFIX,nyt.com,Proxy
DOMAIN-SUFFIX,nytimes.com,Proxy
DOMAIN-SUFFIX,omnigroup.com,Proxy
DOMAIN-SUFFIX,onenote.com,Proxy
DOMAIN-SUFFIX,openvpn.net,Proxy
DOMAIN-SUFFIX,openwrt.org,Proxy
DOMAIN-SUFFIX,origami.design,Proxy
DOMAIN-SUFFIX,ow.ly,Proxy
DOMAIN-SUFFIX,periscope.tv,Proxy
DOMAIN-SUFFIX,playpcesor.com,Proxy
DOMAIN-SUFFIX,pinboard.in,Proxy
DOMAIN-SUFFIX,qdaily.com,Proxy
DOMAIN-SUFFIX,skype.com,Proxy
DOMAIN-SUFFIX,slack-edge.com,Proxy
DOMAIN-SUFFIX,slack.com,Proxy
DOMAIN-SUFFIX,smartmailcloud.com,Proxy
DOMAIN-SUFFIX,sndcdn.com,Proxy
DOMAIN-SUFFIX,soundcloud.com,Proxy
DOMAIN-SUFFIX,sourceforge.net,Proxy,enhanced-mode
DOMAIN-SUFFIX,sourceforge.io,Proxy,enhanced-mode
DOMAIN-SUFFIX,spotify.com,Proxy
DOMAIN-SUFFIX,squarespace.com,Proxy
DOMAIN-SUFFIX,sstatic.net,Proxy
DOMAIN-SUFFIX,stackoverflow.com,Proxy
DOMAIN-SUFFIX,staticflickr.com,Proxy
DOMAIN-SUFFIX,symauth.com,Proxy
DOMAIN-SUFFIX,symcb.com,Proxy
DOMAIN-SUFFIX,symcd.com,Proxy
DOMAIN-SUFFIX,tapbots.com,Proxy
DOMAIN-SUFFIX,tapbots.net,Proxy
DOMAIN-SUFFIX,techcrunch.com,Proxy
DOMAIN-SUFFIX,thepiratebay.org,Proxy
DOMAIN-SUFFIX,tiny.cc,Proxy
DOMAIN-SUFFIX,tinypic.com,Proxy
DOMAIN-SUFFIX,tmblr.co,Proxy
DOMAIN-SUFFIX,tumblr.com,Proxy
DOMAIN-SUFFIX,twitch.tv,Proxy
DOMAIN-SUFFIX,txmblr.com,Proxy
DOMAIN-SUFFIX,typekit.net,Proxy
DOMAIN-SUFFIX,ubnt.com,Proxy
DOMAIN-SUFFIX,urchin.com,Proxy
DOMAIN-SUFFIX,v.gd,Proxy
DOMAIN-SUFFIX,vimeo.com,Proxy
DOMAIN-SUFFIX,vimeocdn.com,Proxy
DOMAIN-SUFFIX,vine.co,Proxy
DOMAIN-SUFFIX,vox-cdn.com,Proxy
DOMAIN-SUFFIX,vsco.co,Proxy
DOMAIN-SUFFIX,weather.com,Proxy
DOMAIN-SUFFIX,wikimedia.org,Proxy
DOMAIN-SUFFIX,wikipedia.com,Proxy
DOMAIN-SUFFIX,wikipedia.org,Proxy
DOMAIN-SUFFIX,windows.net,Proxy
DOMAIN-SUFFIX,wordpress.com,Proxy
DOMAIN-SUFFIX,wp.com,Proxy
DOMAIN-SUFFIX,wsj.com,Proxy
DOMAIN-SUFFIX,wsj.net,Proxy
DOMAIN-SUFFIX,yahoo.com,Proxy
DOMAIN-SUFFIX,youtu.be,Proxy
DOMAIN-SUFFIX,ytimg.com,Proxy

# Telegram
IP-CIDR,91.108.56.0/22,Proxy,no-resolve
IP-CIDR,91.108.4.0/22,Proxy,no-resolve
IP-CIDR,109.239.140.0/24,Proxy,no-resolve
IP-CIDR,149.154.160.0/20,Proxy,no-resolve

# LAN
IP-CIDR,192.168.0.0/16,DIRECT
IP-CIDR,10.0.0.0/8,DIRECT
IP-CIDR,172.16.0.0/12,DIRECT
IP-CIDR,127.0.0.0/8,DIRECT

GEOIP,CN,DIRECT
FINAL,Proxy

[Host]
api.smoot.apple.cn = api.smoot.apple.com

[URL Rewrite]
^http://www.google.cn http://www.google.com
```


<mark>特别注意这里
`随便起个名字 = custom,ip,port,AES-256-CFB,password,https://github.com/weixiubin/ss/blob/master/SSEncrypt.module
`
不要有空格，我试过有空格代理不成功的情况，删除空格就可以了。</mark>
