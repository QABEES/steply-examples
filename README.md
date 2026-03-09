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

## Run a test pack:
```shell
steply -f tests --target-env env/sit1.properties
```

## CI Integration

This project includes a GitHub Actions workflow (`.github/workflows/ci.yml`) that runs automatically on push and pull requests to `main`, 
and can also be triggered manually.

**Workflow: `CI`**
- **Runs on:** `ubuntu-latest`

**Steps:**
1. Checkout the repository
2. Set up Java 17 (Temurin distribution)
3. Install Steply (no-JRE variant, added to `PATH`)
4. Run tests: `steply --scenario tests/get_user_api.json --target-env env/sit1.properties`

You can also trigger the workflow manually via the **Actions** tab using `workflow_dispatch`.

## CI Status with your changes (Collaborate here 🤝)
See last successful CI runs here:
- CI Job Link: https://github.com/QABEES/steply-examples/actions
- For any changes(or new example scenario) raise a PR and see your changes being built [here](https://github.com/QABEES/steply-examples/actions). 👈

## CI Status Example:
<details>
<summary>CI Build Passed ✅️ ◀ (Click to expand)</summary>
<img width="2040" height="1266" alt="image" src="https://github.com/user-attachments/assets/aa241091-e326-4217-b209-4906550aec53" />
</details>

## CI Status(Java 17, 21, 25 LTS):
<details>
<summary>CI Last Passed(Java17, Java21, Java25) ✅️ ◀ (Click to expand)</summary>
<img width="1830" height="1354" alt="image" src="https://github.com/user-attachments/assets/687e92c5-cc22-48f5-aec3-ccc3bc924117" />
</details>

## Sample output:
<details>
<summary>Test Console Output ◀ (Click to expand)</summary>

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

