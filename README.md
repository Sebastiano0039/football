Pour que le site se connecte à la base de données et fonctionne correctement, il faut créer un fichier **wp-config.php** à la racine du site, puis y copier/coller le contenu suivant :

(Ne pas oublier de remplacer les mots clefs suivants - chevrons compris :
- BDD_NAME = Nom de la base de données
- USER = Login pour se connecter à la BDD
- PASSWORD = Le mot de passe associé à ce login
- HOST = L'adresse qui héberge le serveur, le plus souvent c'est _localhost_
)

Fichier wp-content :

`<?php
/**
 * La configuration de base de votre installation WordPress.
 *
 * Ce fichier est utilisé par le script de création de wp-config.php pendant
 * le processus d’installation. Vous n’avez pas à utiliser le site web, vous
 * pouvez simplement renommer ce fichier en « wp-config.php » et remplir les
 * valeurs.
 *
 * Ce fichier contient les réglages de configuration suivants :
 *
 * Réglages MySQL
 * Préfixe de table
 * Clés secrètes
 * Langue utilisée
 * ABSPATH
 *
 * @link https://fr.wordpress.org/support/article/editing-wp-config-php/.
 *
 * @package WordPress
 */

// ** Réglages MySQL - Votre hébergeur doit vous fournir ces informations. ** //
/** Nom de la base de données de WordPress. */
define( 'DB_NAME', 'BDD_NAME' );

/** Utilisateur de la base de données MySQL. */
define( 'DB_USER', 'USER' );

/** Mot de passe de la base de données MySQL. */
define( 'DB_PASSWORD', 'PASSWORD' );

/** Adresse de l’hébergement MySQL. */
define( 'DB_HOST', 'HOST' );

/** Jeu de caractères à utiliser par la base de données lors de la création des tables. */
define( 'DB_CHARSET', 'utf8mb4' );

/**
 * Type de collation de la base de données.
 * N’y touchez que si vous savez ce que vous faites.
 */
define( 'DB_COLLATE', '' );

/**#@+
 * Clés uniques d’authentification et salage.
 *
 * Remplacez les valeurs par défaut par des phrases uniques !
 * Vous pouvez générer des phrases aléatoires en utilisant
 * {@link https://api.wordpress.org/secret-key/1.1/salt/ le service de clés secrètes de WordPress.org}.
 * Vous pouvez modifier ces phrases à n’importe quel moment, afin d’invalider tous les cookies existants.
 * Cela forcera également tous les utilisateurs à se reconnecter.
 *
 * @since 2.6.0
 */
define( 'AUTH_KEY',         'FwOtkNA9T{59b *DBc_4`v5(|$Uxe7Kd`-E1zLc{}v97Q:P_s%m;]:& W4Fu>GqI' );
define( 'SECURE_AUTH_KEY',  'SC;M2NOpTpmJz8S?o=%A`If4Lno~l?3I-A|uIQ@KMLRx?c[qN::I|tS~GW?d,znl' );
define( 'LOGGED_IN_KEY',    '8X${m2e9jM(+0d3PoAy J5vFf[dNUt>HW.OXk{{[77[2%658&76dws}naYFJ{!:t' );
define( 'NONCE_KEY',        '5Z$y$2_Ib?I0YNP&YWs{=zunM5=MAZwkbK9O<!~NGqvqUUZ@w>SJ/(DsG8FB&U;Z' );
define( 'AUTH_SALT',        'm5~0R^T$/?RK/Z)k>N%rH/k8>3u+GM@>*[sldpJk`@WamcG>i5CC44;9^_ui;xON' );
define( 'SECURE_AUTH_SALT', 'w0Meh}!~fu~03KY .s1_+/iEevfvKN%L&77@{iqHef05yB0zJ@BdkcOpEMn/`;=}' );
define( 'LOGGED_IN_SALT',   'm^F=l5r~@/bXGtA@LGfk$Q!hdQ?1.Ub4p^km+5ft9+ULME%*#}Z3R(qSy/`uQ  L' );
define( 'NONCE_SALT',       'Va6QS0W<)N-A9DY`&rvfcbPf41|PfVw}edF~tDt &#F_PB-lBwzfCvHnc#09oT[8' );
/**#@-*/

/**
 * Préfixe de base de données pour les tables de WordPress.
 *
 * Vous pouvez installer plusieurs WordPress sur une seule base de données
 * si vous leur donnez chacune un préfixe unique.
 * N’utilisez que des chiffres, des lettres non-accentuées, et des caractères soulignés !
 */
$table_prefix = 'foot_';

/**
 * Pour les développeurs : le mode déboguage de WordPress.
 *
 * En passant la valeur suivante à "true", vous activez l’affichage des
 * notifications d’erreurs pendant vos essais.
 * Il est fortement recommandé que les développeurs d’extensions et
 * de thèmes se servent de WP_DEBUG dans leur environnement de
 * développement.
 *
 * Pour plus d’information sur les autres constantes qui peuvent être utilisées
 * pour le déboguage, rendez-vous sur le Codex.
 *
 * @link https://fr.wordpress.org/support/article/debugging-in-wordpress/
 */
define( 'WP_DEBUG', false );

/* C’est tout, ne touchez pas à ce qui suit ! Bonne publication. */

/** Chemin absolu vers le dossier de WordPress. */
if ( ! defined( 'ABSPATH' ) )
  define( 'ABSPATH', dirname( __FILE__ ) . '/' );

/** Réglage des variables de WordPress et de ses fichiers inclus. */
require_once( ABSPATH . 'wp-settings.php' );`
