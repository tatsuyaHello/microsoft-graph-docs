---
description: "Automatically generated file. DO NOT MODIFY"
---

```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/organization/d69179bf-f4a4-41a9-a9de-249c0f2efb1d/branding/localizations/signInPageText"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
	completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

		MSGraphOrganizationalBrandingLocalization *organizationalBrandingLocalization = [[MSGraphOrganizationalBrandingLocalization alloc] initWithData:data error:&nserror];

}];

[meDataTask execute];

```