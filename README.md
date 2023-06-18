<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## LARAVEL MIX
- npm install
- npm init -y
- npm install laravel-mix --save-dev
- create file in the root => webpack.mix.js :
    add : const mix = require("laravel-mix");

            mix.js("resources/js/app.js", "public/js");
            mix.webpackConfig({
                resolve: {
                    extensions: ["*", ".wasm", ".mjs", ".js", ".jsx", ".json"],
                },
            });


- change to at package.json => "scripts": {
  "dev": "npm run development",
  "development": "mix",
  "watch": "mix watch",
  "hot": "mix watch --hot",
  "prod": "npm run production",
  "production": "mix --production"
}
- delete type in pakcage.json
- npx mix