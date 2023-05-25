I recently faced an issue where I needed to upgrage a laravel project to laravel 8 but the zizaco/entrust package was only available upto laravel 5.8. This is how I got around that issue.

1. Add the following repository in composer.json file:
"repositories": [
    {
        "type": "path",
        "url": "packages/zizaco/entrust"
    },
],

2. Add the package dependency in require section of composer.json file:
"zizaco/entrust": "dev-master",

3. Clone this repository and paste it in your project root/packages/zizaco/entrust.

4. upgrade your project version and run composer update. This will work upto laravel 8. 