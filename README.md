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
3. docker compose -f docker-compose-first.yml up -d
4. docker compose -f docker-compose-first.yml exec l9vitedev-app bash
5. composer create-project "laravel/laravel=9.*" l9vitedev_tmp --prefer-dist
8. rm l9vitedev_tmp/README.md l9vitedev_tmp/vite.config.js -rf
6. mv l9vitedev_tmp/* ./
7. mv l9vitedev_tmp/.* ./
8. rm l9vitedev_tmp -rf
9. mkdir ./docker/nginx/logs
10. exit
11. docker compose -f docker-compose-second.yml down
12. docker compose -f docker-compose-second.yml up -d
13. docker compose -f docker-compose-second.yml exec l9vitedev-app bash
14. npm install
15. composer install
16. npm run dev
17. chmod -R guo+w storage
18. php artisan storage:link
19. [vite 起動確認](http://localhost:5173)
20. [laravel 起動確認](http://localhost)