share

qq，微信，微博等分享做了处理
使用方式：
1.将文件导入项目 2.调用相应的接口
if (index==0) {
    QQShare *qqShare = [QQShare sharedInstance];
    [qqShare sharedMessageToQQ:nil title:self.todayNews.newsTitle detailUrl:self.todayNews.newsUrl imageData:imageData shareType:QQMessage];
}else if(index==1){
SinaWeiboShare *sinaWeiboShare = [SinaWeiboShare sharedInstance];
[sinaWeiboShare sharedMessageToSinaWeibo:sharedContent
                                   imageData:imageData];
}else if (index==2){
    TencentWeixinShare *tencentWeixinShare = [TencentWeixinShare sharedInstance];
// [tencentWeixinShare sharedMessageToTencentWeixin:sharedContent imageData:imageData messageType:WXSession];
// [tencentWeixinShare sharedMessageToTencentWeixin:sharedContent imageData:imageData webpageUrl:self.todayNews.newsUrl messageType:WXSession];
    [tencentWeixinShare sharedMessageToTencentWeixin:@"文字" imageData:imageData wxtitle:self.todayNews.newsTitle webpageUrl:self.todayNews.newsUrl messageType:WXSession];
}else if(index==3){
TencentWeixinShare *tencentWeixinShare = [TencentWeixinShare sharedInstance];
[tencentWeixinShare sharedMessageToTencentWeixin:
                                           @"文字"imageData:imageData wxtitle:self.todayNews.newsTitle webpageUrl:self.todayNews.newsUrl messageType:WXTimeline];
                                           }
