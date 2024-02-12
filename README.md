<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## 概要

laravel9 vite 環境構築
- [(参考) Laravel 9 + VITEの開発環境をdockerで実現する方法](https://qiita.com/hitotch/items/aa319c49d625c2a9b65e).

1. git clone https://github.com/engineer-mogura/l9vitedev.git
2. cd l9vitedev
3. docker compose up -d
4. docker compose exec l9vitedev-app bash
5. composer create-project "laravel/laravel=9.*" l9vitedev_tmp --prefer-dist
6. mv l9vitedev_tmp/* ./
7. mv l9vitedev_tmp/.* ./
8. rm l9vitedev_tmp -rf
9. chmod -R guo+w storage
10. php artisan storage:link
11. npm install
12. composer install
13. npm run dev
14. [vite 起動確認](http://localhost:5173)
15. [laravel 起動確認](http://localhost)