# Zhaitos Browser

Navegador para Windows basado en Microsoft Edge WebView2, centrado en la privacidad, el bajo consumo de recursos y una biblioteca integrada de manga, manhwa, anime y donghua.

## Funciones

- **Escudo de privacidad:** bloqueo de anuncios y rastreadores, protección contra fingerprinting, HTTPS obligatorio, DNS cifrado y protección WebRTC.
- **Escudo de descargas:** ninguna página puede descargar archivos sin tu permiso. Cada descarga se analiza con el antivirus de Windows y las amenazas se aíslan en cuarentena.
- **Bóveda cifrada:** contraseñas y datos personales protegidos con tu cuenta de Windows (DPAPI).
- **Rendimiento adaptativo:** las pestañas inactivas se duermen y liberan memoria según los recursos de tu PC.
- **Biblioteca:** catálogo de manga (MangaDex) y anime (MyAnimeList), lector integrado, progreso de lectura y disponibilidad en las fuentes que configures.
- **Actualizaciones verificadas:** comprobación de integridad (SHA-256) y vuelta automática a la versión anterior si algo falla.

## Requisitos

- Windows 10 (versión 2004 o posterior) o Windows 11, de 64 bits.
- [SDK de .NET 8](https://dotnet.microsoft.com/download/dotnet/8.0): el instalador compila el navegador en tu equipo.
- Microsoft Edge WebView2 Runtime. Si no lo tienes, el instalador lo instala.

### Instalar el SDK de .NET 8 desde CMD

1. Abre **Símbolo del sistema** (CMD) o **PowerShell**.
2. Ejecuta:

   ```cmd
   winget install Microsoft.DotNet.SDK.8
   ```

3. Acepta los términos si te los pide y espera a que termine.
4. **Cierra y vuelve a abrir** la ventana de CMD, y comprueba que quedó instalado:

   ```cmd
   dotnet --list-sdks
   ```

   Debe aparecer una línea que empiece por `8.`.

Si `winget` no existe en tu equipo, instala **Instalador de aplicación** desde Microsoft Store, o descarga el SDK desde la [página oficial de .NET 8](https://dotnet.microsoft.com/download/dotnet/8.0) (elige **SDK 8.x · Windows · x64**).

## Instalación

1. Descarga `Instalar_ZhaidBrowser_XX.cmd` de la [última versión](https://github.com/Sr343/Zhaitos-Browser/releases/latest).
2. Ejecútalo y acepta los permisos de administrador.
3. La compilación tarda entre 1 y 3 minutos.

Para actualizar, ve al menú ⋯ y pulsa **Buscar actualizaciones…**.

## Privacidad

Tus contraseñas, historial, sesiones y ajustes se guardan solo en tu equipo, cifrados. Este repositorio no recibe ni almacena datos de ningún usuario.

## Aviso

Zhaitos Browser no aloja ningún contenido. La biblioteca muestra información pública y enlaces a sitios de terceros elegidos por el usuario, que es responsable de usarlos conforme a la ley de su país.
