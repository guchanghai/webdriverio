# webdriverio
[webdriverio](https://webdriver.io/) learning notes

<img width="219" alt="image" src="https://github.com/guchanghai/webdriverio/assets/2970098/0de399fa-b703-4409-a416-0cc344054086">

# Best practice

https://webdriver.io/docs/bestpractices

```ts
// 👍
await expect(button).toBeDisplayed()
```

```ts
// 👍
await button.click()

// 👍
await expect(button).toHaveText('Submit')
```

# item

## selector

https://webdriver.io/docs/selectors

<img width="994" alt="image" src="https://github.com/guchanghai/webdriverio/assets/2970098/f3002aa8-c925-4c89-a85c-5511f28d6ad0">

## timeout

https://webdriver.io/docs/timeouts

|item|default timeout (seconds)|Change|
|:-|:-:|:-|
| script | 30 | `await browser.setTimeout({ 'script': 60000 })` |
| test | 10 | By default, the timeout is 10 seconds, which means that a single test should not take longer than that.|

## Run Selected Tests

For example, to run only your login test:

```sh
wdio wdio.conf.js --spec ./test/specs/e2e/login.js
```

Or run multiple specs at once:

```sh
wdio wdio.conf.js --spec ./test/specs/signup.js --spec ./test/specs/forgot-password.js
```


