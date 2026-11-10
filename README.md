# Zhaitos Browser

**Zhaitos Browser** es un navegador para Windows basado en Microsoft Edge WebView2, centrado en privacidad, seguridad, bajo consumo de recursos y una Biblioteca integrada para manga, manhwa, anime y donghua.

> Actualmente Zhaitos Browser está en desarrollo activo. Las versiones publicadas deben considerarse beta.

## Características

###  Escudo de privacidad

- Bloqueo de anuncios y rastreadores.
- Protección contra fingerprinting.
- Protección WebRTC.
- HTTPS obligatorio.
- Global Privacy Control.
- Limpieza de parámetros de seguimiento.
- DNS cifrado.
- Bloqueo de ventanas emergentes.
- Excepciones configurables por sitio.
- Modo privado.

###  Escudo de descargas

Zhaitos puede impedir que una página inicie una descarga sin autorización.

Incluye:

- Modo **Estricto**.
- Modo **Riesgosas**.
- Modo **Libre**.
- Confirmación antes de permitir descargas.
- Protección adicional para EXE, MSI, CMD, BAT, PowerShell y otros formatos ejecutables.
- Historial de intentos bloqueados.
- Sitios permitidos configurables.
- Análisis local mediante Microsoft Defender.
- Cuarentena de archivos detectados como amenaza.
- Cálculo SHA-256 de archivos descargados.

Los archivos no se envían a servicios externos para realizar el análisis.

---

##  Bóveda cifrada

Zhaitos protege contraseñas y datos locales mediante **Windows DPAPI**.

La protección queda asociada a la cuenta de Windows del usuario.

La información sensible se mantiene localmente y no se sincroniza automáticamente con servidores externos.

---

##  Rendimiento adaptativo

Zhaitos supervisa los recursos disponibles del equipo y adapta su comportamiento automáticamente.

Perfiles disponibles:

- Protección del sistema.
- Ultra ligero.
- Ahorro.
- Equilibrado.
- Rendimiento.
- Alto rendimiento.

### Pestañas dormidas

Una pestaña inactiva puede pasar a:

```text
zz
```

Esto indica que WebView2 ha suspendido la pestaña para reducir CPU y consumo de recursos.

### Pestañas liberadas

Cuando existe presión prolongada de memoria, Zhaitos puede pasar una pestaña a:

```text
zZ
```

En este estado:

- La página se descarga de memoria.
- Se conserva la URL.
- Se conserva el título.
- Se conserva la posición aproximada de desplazamiento.
- La pestaña se restaura cuando vuelves a utilizarla.

Puedes configurar sitios que **nunca deben dormirse**, por ejemplo servicios de música, streaming o comunicación.

---

#  Zhaitos Biblioteca

La Biblioteca permite organizar y consultar manga, manhwa, anime y donghua desde el navegador.

## Manga / Manhwa

Incluye integración con fuentes como:

- MangaDex.
- Fuentes web configurables.
- Seguimiento de progreso.
- Lector integrado.
- Capítulos.
- Portadas.
- Diagnóstico de conectores.
- Caché y recuperación ante fallos.

## Anime

MyAnimeList se utiliza como catálogo principal.

La Biblioteca puede comprobar disponibilidad entre diferentes proveedores configurados y distinguir:

- Títulos.
- Sinónimos.
- Temporadas.
- Movies.
- OVA / OAD.
- Specials.
- Parts / Cours.

También puede mostrar información de emisión cuando MyAnimeList proporciona un horario válido.

## Donghua

La Biblioteca incluye una sección separada para animación china y conectores específicos.

---

#  Diagnóstico de conectores

En:

```text
Biblioteca → Ajustes → Estado de conectores
```

puedes comprobar:

- Fuente.
- Estado.
- Última respuesta correcta.
- Último error.
- Fallos consecutivos.

También es posible generar archivos de diagnóstico para analizar cambios en sitios externos sin ejecutar sus scripts.

---

#  Actualizaciones

Zhaitos consulta automáticamente:

```text
https://github.com/Sr343/Zhaitos-Browser/releases/latest/download/zhaid-update.json
```

El navegador puede:

1. Detectar una nueva versión.
2. Descargar el instalador.
3. Comprobar su SHA-256.
4. Crear una copia de la versión instalada.
5. Instalar la nueva versión.
6. Comprobar que Zhaitos arranque correctamente.
7. Restaurar automáticamente la versión anterior si la nueva instalación falla.

También puedes comprobar manualmente desde:

```text
Menú → Ajustes → Buscar actualizaciones…
```

---

#  Instalación recomendada

## ZhaitosBrowserSetup.exe

La forma recomendada de instalar Zhaitos es descargar:

```text
ZhaitosBrowserSetup.exe
```

desde la [última release](https://github.com/Sr343/Zhaitos-Browser/releases/latest).

El Setup funciona como un instalador puente.

Automáticamente:

1. Comprueba si existe el SDK de .NET 8.
2. Si falta, intenta instalarlo mediante WinGet.
3. Si WinGet no está disponible, utiliza el instalador oficial de Microsoft como respaldo.
4. Consulta la última versión publicada en GitHub.
5. Descarga el instalador correspondiente.
6. Comprueba su SHA-256.
7. Solo ejecuta el instalador si la verificación de integridad es correcta.

De esta forma el mismo:

```text
ZhaitosBrowserSetup.exe
```

puede utilizarse para instalar futuras versiones.

---

#  Requisitos

- Windows 10 x64.
- Windows 11 x64.
- Microsoft Edge WebView2 Runtime.
- SDK de .NET 8.

El Setup puede instalar automáticamente .NET 8 cuando no está disponible.

---

## Instalar manualmente .NET 8

Si deseas instalar el SDK manualmente, abre CMD o PowerShell:

```cmd
winget install --id Microsoft.DotNet.SDK.8 --exact
```

Después cierra y vuelve a abrir la consola y comprueba:

```cmd
dotnet --list-sdks
```

Debe aparecer alguna versión que empiece por:

```text
8.
```

También puedes descargarlo desde:

https://dotnet.microsoft.com/download/dotnet/8.0

---

#  Instalación avanzada

Los usuarios que prefieran el instalador tradicional pueden descargar:

```text
Instalar_ZhaitosBrowser_XX.cmd
```

desde Releases.

Este método:

- Compila Zhaitos en el equipo.
- Instala los componentes necesarios.
- Permite 
