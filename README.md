# steply-examples
Sample tests using [Steply](https://github.com/QABEES/steply) CLI

## Install Steply
```shell
curl -fsSL https://raw.githubusercontent.com/QABEES/steply/main/scripts/install.sh | bash
```

## Run a test:
```shell
steply --scenario tests/get_user_api.json --target-env env/sit1.properties
```
## Sample output:

<details>
<summary>Console Output ◀ (Click to expand)</summary>

```js
➜  steply-examples git:(main) ✗ steply --scenario tests/get_user_api.json --target-env env/sit1.properties 

2026-03-05 10:01:14,603 [main]: 
-----------------------------------------------------------------------------------

Scenario:
+++++++++

GET GITHUB USER DETAILS AND VALIDATE RESPONSE 

-----------------------------------------------------------------------------------

--------- TEST-STEP-CORRELATION-ID: 9d678507-8c7b-480a-98ed-9b6665e99fd9 ---------
*requestTimeStamp:2026-03-05T10:01:14.647
step:get_user_details
url:https://api.github.com/users/octocat
method:GET
request:
{ } 
--------- TEST-STEP-CORRELATION-ID: 9d678507-8c7b-480a-98ed-9b6665e99fd9 ---------
Response:
{
  "status" : 200,
  "headers" : {
    "Accept-Ranges" : [ "bytes" ],
    "Access-Control-Allow-Origin" : [ "*" ],
    "Access-Control-Expose-Headers" : [ "ETag, Link, Location, Retry-After, X-GitHub-OTP, X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Used, X-RateLimit-Resource, X-RateLimit-Reset, X-OAuth-Scopes, X-Accepted-OAuth-Scopes, X-Poll-Interval, X-GitHub-Media-Type, X-GitHub-SSO, X-GitHub-Request-Id, Deprecation, Sunset" ],
    "Cache-Control" : [ "public, max-age=60, s-maxage=60" ],
    "Content-Security-Policy" : [ "default-src 'none'" ],
    "Content-Type" : [ "application/json; charset=utf-8" ],
    "Date" : [ "Thu, 05 Mar 2026 10:01:14 GMT" ],
    "ETag" : [ "W/\"8559416ef35e3eec89015b24849a5b6206e831b49e11cfec04e6b240f1837efd\"" ],
    "Last-Modified" : [ "Sun, 22 Feb 2026 12:22:52 GMT" ],
    "Referrer-Policy" : [ "origin-when-cross-origin, strict-origin-when-cross-origin" ],
    "Server" : [ "github.com" ],
    "Strict-Transport-Security" : [ "max-age=31536000; includeSubdomains; preload" ],
    "Vary" : [ "Accept,Accept-Encoding, Accept, X-Requested-With" ],
    "X-Content-Type-Options" : [ "nosniff" ],
    "X-Frame-Options" : [ "deny" ],
    "x-github-api-version-selected" : [ "2022-11-28" ],
    "X-GitHub-Media-Type" : [ "github.v3; format=json" ],
    "X-GitHub-Request-Id" : [ "B646:3E30C6:703151:87B13E:69A9546A" ],
    "X-RateLimit-Limit" : [ "60" ],
    "X-RateLimit-Remaining" : [ "59" ],
    "X-RateLimit-Reset" : [ "1772708474" ],
    "X-RateLimit-Resource" : [ "core" ],
    "X-RateLimit-Used" : [ "1" ],
    "X-XSS-Protection" : [ "0" ]
  },
  "body" : {
    "login" : "octocat",
    "id" : 583231,
    "node_id" : "MDQ6VXNlcjU4MzIzMQ==",
    "avatar_url" : "https://avatars.githubusercontent.com/u/583231?v=4",
    "gravatar_id" : "",
    "url" : "https://api.github.com/users/octocat",
    "html_url" : "https://github.com/octocat",
    "followers_url" : "https://api.github.com/users/octocat/followers",
    "following_url" : "https://api.github.com/users/octocat/following{/other_user}",
    "gists_url" : "https://api.github.com/users/octocat/gists{/gist_id}",
    "starred_url" : "https://api.github.com/users/octocat/starred{/owner}{/repo}",
    "subscriptions_url" : "https://api.github.com/users/octocat/subscriptions",
    "organizations_url" : "https://api.github.com/users/octocat/orgs",
    "repos_url" : "https://api.github.com/users/octocat/repos",
    "events_url" : "https://api.github.com/users/octocat/events{/privacy}",
    "received_events_url" : "https://api.github.com/users/octocat/received_events",
    "type" : "User",
    "user_view_type" : "public",
    "site_admin" : false,
    "name" : "The Octocat",
    "company" : "@github",
    "blog" : "https://github.blog",
    "location" : "San Francisco",
    "email" : null,
    "hireable" : null,
    "bio" : null,
    "twitter_username" : null,
    "public_repos" : 8,
    "public_gists" : 8,
    "followers" : 21973,
    "following" : 9,
    "created_at" : "2011-01-25T18:44:36Z",
    "updated_at" : "2026-02-22T12:22:52Z"
  }
}
*responseTimeStamp:2026-03-05T10:01:15.023 
*Response delay:376.0 milli-secs 
---------> Expected Response: <----------
{
  "status" : 200,
  "body" : {
    "login" : "octocat",
    "id" : 583231,
    "type" : "User"
  }
} 
 
-done-

------------------------------------------------------------------------------------------------
SUMMARY:
--------
Run count: 1
Failure count: 0
------------------------------------------------------------------------------------------------
✅ Tests passed
➜  steply-examples git:(main) ✗ 
```

</details>

