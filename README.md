# Introduction
1. Intro
Cette configuration n'est donc PAS une couverture de tous les cas d'utilisation. (Si c'est ce que vous recherchez, peut-être que quelque chose comme Devilbox , PHPDocker.io ou Laradock pourrait mieux répondre à vos besoins.)
 Ce n'est pas "optimisé pour l'ultra-vitesse". Mais c'est plutôt un point de départ,
 et il a à l'esprit l'expérience du développeur, la simplicité et la facilité de compréhension.
 C'est pourquoi j'essaie aussi d'utiliser autant que possible des éléments "prêts à l'emploi",
 stables et "ennuyeux", au lieu d'emballer, d'automatiser et d'optimiser chaque bit
 (par exemple, c'est pourquoi j'utilise simplement PHP-FPM au lieu de quelque chose
 comme Alpine pour la configuration de base - mais bien sûr,
 vous pouvez la changer pour celle avec laquelle vous vous sentez le plus à l'aise).

# inclure dans l'application docker :

- PHP-FPM (à partir de maintenant, version 7.4 ; inclut quelques extensions supplémentaires (telles que bcmath), zsh, oh-my-zsh et le thème powerlevel10k
- Base de données PostgreSQL (à partir de maintenant, version 12), y compris une base de données pour les tests
- Serveur nginx

2. PHP-FPM et le Dockerfile:
php-fpmNous utilisons une configuration simple pour l'application principale. C'est le Dockerfile,
où nous pouvons ajouter des commandes et exécuter certaines choses en fonction de l' php-fpmimage.
