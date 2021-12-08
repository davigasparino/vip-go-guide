# Configurações VIP GO

*Documentação: (https://wpvip.com/documentation/vip-go/local-vip-go-development-environment)

1 - Agora dentro do diretório acessar public_html/ e remover pasta wp-content.
```
rm -r wp-content 
```

2 - Clone o wp-content do repositório abril-vip-go.
```
git clone {repositório} wp-content
```

3 - Altere o arquivo wp-config inserindo este código:
```
  define( 'DISALLOW_FILE_EDIT', true );
  define( 'DISALLOW_FILE_MODS', true );
  define( 'AUTOMATIC_UPDATER_DISABLED', true );
  define( 'JETPACK_DEV_DEBUG', true );

  define( 'WP_DEBUG', false );
  define( 'SCRIPT_DEBUG', true );
  define( 'WP_DEBUG_LOG', 'tmp/wp-errors.log' );
  if ( file_exists( __FILE__ . '/wp-content/vip-config/vip-config.php' ) ) {
	  require_once( __FILE__ . '/wp-content/vip-config/vip-config.php' );
  }
```
4 - Baixe os plugins da automatic
``` 
git clone git@github.com:Automattic/vip-go-mu-plugins.git mu-plugins --recursive
```
