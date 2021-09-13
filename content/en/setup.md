---
title: Add your First Router
description: ''
position: 2
category: Getting Started
requirements:
  - API service should be enabled in /ip service
  - API-SSL service should be disabled. AutomaTik will configure and enable it.
  - You need to give access to AutomaTik servers. Just copy paste below commands in your terminal window.
---

<!-- Check the [Nuxt.js documentation](https://nuxtjs.org/guides/configuration-glossary/configuration-modules) for more information about installing and using modules in Nuxt.js. -->

<!-- ## Installation

Add `@nuxtjs/xxx` dependency to your project:

<code-group>
  <code-block label="Yarn" active>

  ```bash
  yarn add @nuxtjs/xxx
  ```

  </code-block>
  <code-block label="NPM">

  ```bash
  npm install @nuxtjs/xxx
  ```

  </code-block>
</code-group> -->

<!-- Then, add `@nuxtjs/xxx` to the `modules` section of `nuxt.config.js`:

```js[nuxt.config.js]
{
  modules: [
    '@nuxtjs/xxx'
  ],
  xxx: {
    // Options
  }
}
``` -->

## Requirements
<list :items="requirements"></list>


```
/ip firewall filter
add action=accept chain=input src-address=207.154.253.139 comment=AutomaTik
add action=accept chain=input src-address=157.230.98.182 comment=AutomaTik
```
<alert type="warning">
Please make sure these rules above are not added after your 'ANY ANY DROP' rule if you have one... If you don't have such a rule consider having one.
</alert>

## Add new Router
After logging in your dashboard, click + button to begin adding your first router.

<img src='ss/add_new_router.png'>

You need to fill in a simple form. 
<alert type="warning">
Username password information in this form will be used temporarily.
You can change the password or completely delete this user after this process.
</alert>

## Fill in the form
<img src="ss/temp_user_pass.png">

Next window, you will see AutomaTik will configure API-SSL and SSH service on your router.
If successful, you should see a window like this:


## Finish 

<img src="ss/finish.png">

If there is an error message, you will see the reason why it failed. 

Click 'FINISH' to complete this process.

<alert type="warning">
You may have a message saying 'TRY AGAIN LATER', if this happens please refresh your browser and try again. AutomaTik is still in BETA.
</alert>

Now, you should be able to see your router added on your dashboard.

<img src="ss/router_added.png">
