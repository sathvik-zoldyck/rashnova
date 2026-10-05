<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova, la caja negra de tu portátil, de Alcyone Secure" width="100%">

# Rashnova

### Un registrador de actividad para Windows que deja ver cualquier manipulación

**Entrega tu PC. Recíbelo con un registro sellado de lo que se hizo con él.**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**Descargar**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**Sitio web**](https://www.alcyonesecure.com) ·
[**Límites conocidos**](KNOWN_LIMITS.md) ·
[**Privacidad**](#privacy) ·
[**Seguridad**](SECURITY.md)

</div>

> **Idiomas** &nbsp;·&nbsp; [English](README.md) · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · **Español** · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português](README.pt.md) · [日本語](README.ja.md) · [Bahasa Indonesia](README.id.md) · [עברית](README.he.md)

---
> [!NOTE]
> Esta página está traducida del inglés. La aplicación Rashnova está en inglés, por eso los nombres de botones y
> pantallas aparecen aquí en inglés. Si esta página y la [versión en inglés](README.md) difieren, vale la versión en inglés.


Rashnova registra lo que ocurre en un PC con Windows mientras lo tiene otra persona: en un taller de reparación,
en el departamento de informática o con cualquiera a quien se lo entregues. Inicia una **Repair session** antes de
entregarlo. Cuando el PC vuelva, termínala, y Rashnova te da un veredicto y un informe de lo que se abrió, copió,
renombró y borró, qué programas se ejecutaron y qué unidades USB se conectaron.

Cada entrada queda sellada a la anterior, así que el registro muestra si algo se alteró o se eliminó, y muestra
cada intervalo en el que no se pudo registrar nada. Todo se queda en tu ordenador. Sin cuenta, sin nube, sin telemetría.


> [!NOTE]
> Este repositorio es donde se **publica** Rashnova: instaladores, notas de versión, límites conocidos y política de
> seguridad. Rashnova es software propietario de [Alcyone Secure](https://www.alcyonesecure.com); su código fuente no se
> publica aquí.


## Contenido

- [Por qué existe Rashnova](#why)
- [Qué hace](#what-it-does)
- [Lo que nunca registra](#never)
- [Cómo funciona](#how)
- [Descarga e instalación](#download)
- [Requisitos del sistema](#requirements)
- [Privacidad](#privacy)
- [Límites conocidos](#limits)
- [Actualizaciones](#updates)
- [Ayuda y seguridad](#support)
- [Licencia](#licence)

<a name="why"></a>
## Por qué existe Rashnova

Los aviones, los trenes y los barcos llevan una caja negra. Un ordenador que sale de tus manos no lleva nada,
y quien lo tiene accede a todo lo que hay en él.

Y ese acceso se usa. En un [estudio de 2022 de investigadores de la Universidad de Guelph](https://arxiv.org/abs/2211.05824)
(publicado en el IEEE Symposium on Security and Privacy 2023), se dejaron portátiles durante una noche en 12 talleres de
reparación con el registro activado. Los técnicos de seis de ellos accedieron a los datos personales que contenían, y dos
copiaron datos del portátil. Los antivirus y las herramientas de endpoint nunca se diseñaron para notar esto: a esa
persona se le entregaron las llaves.

Rashnova no es prevención. Es evidencia, para que lo ocurrido se pueda comprobar en lugar de discutir.

> *La confianza está bien. La prueba, mejor.*

<a name="what-it-does"></a>
## Qué hace

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode (modo reparación).** Una sesión vigilada, que se inicia con tu PIN antes de la entrega y se termina
con tu PIN cuando recuperas el PC. Registra los archivos abiertos, creados, renombrados, copiados y borrados, los
programas iniciados, los comandos de PowerShell ejecutados, los inicios de sesión y el almacenamiento USB conectado,
incluido cada archivo escrito en él. Un reinicio, un apagado o la suspensión nunca terminan la sesión: el informe
muestra cada interrupción y cuánto duró.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="Resumen de sesión: un veredicto, los eventos más destacados y la comprobación de la cadena">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="Explorador de sesión: cada evento a lo largo del tiempo, por programa y por carpeta">

</td>
<td width="50%" valign="top">

**Un registro que puedes comprobar.** Cada sesión termina con un veredicto y un informe que puedes guardar como
PDF, página web u hoja de cálculo. El explorador de sesión muestra cada evento a lo largo del tiempo, por programa y por
carpeta, y la comprobación de la cadena te dice si el registro está intacto. Lo que guardas es una copia; el original se
queda donde Rashnova lo guarda.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**El Readout semanal.** Tu semana en un veredicto, con como mucho unas pocas cosas que conviene mirar. Marca cada
una como "that was me" (fui yo) o "that wasn't me" (no fui yo). También dice, con palabras sencillas, qué puede ver
Rashnova y qué no.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="El Readout semanal: un veredicto de la semana, cosas que conviene mirar, actividad por día">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="La elección entre grabar solo en sesiones o siempre">

</td>
<td width="50%" valign="top">

**Grabación continua (always-on), solo si la eliges.** Desactivada hasta que la actives. Guarda lo irreversible y
lo alarmante (borrados permanentes, archivos de aspecto sensible, cualquier cosa que entre o salga de una unidad
extraíble), no tu uso diario de tus propios archivos. Desactivarla es un clic desde la bandeja o Settings, y nunca
necesita tu PIN.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Desde la bandeja.** Comprueba que una sesión está grabando, termínala, haz una comprobación de 30 segundos de la
actividad de archivos en directo (Monitor Now) o abre el último informe.

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="El panel rápido en la bandeja de Windows" width="70%">

</td>
</tr>
</table>

<sub>Las capturas muestran Rashnova con una sesión de ejemplo (una usuaria ficticia, "Riya").</sub>

**Novedades de 1.2.0:** Handover Mode, para prestar tu PC a tu familia, a un amigo o a un compañero, con el mismo
informe sellado; bloqueo de almacenamiento USB; y Start with Windows. Consulta el [registro de cambios](CHANGELOG.md).

<a name="never"></a>
## Lo que nunca registra

Rashnova registra **que** algo ocurrió, no lo que había en la pantalla. No registra:

- pulsaciones de teclas
- el contenido del portapapeles
- tu pantalla, ni en imágenes ni en vídeo
- tu cámara ni tu micrófono
- el contenido de tus documentos, fotos, correos o mensajes
- las páginas web que visitas, ni lo que hay en ellas

Conviene saber dos cosas que sí registra. Durante una Repair session, los comandos de PowerShell se registran al
ejecutarse, y también la línea de arranque completa de cada programa que inicia una persona; así, un navegador abierto
desde un enlace muestra ese enlace.

Un informe dice, por ejemplo, que `Bank_Statement_Aug2026.pdf` se abrió desde `Documents\Finance` con
Microsoft Edge a las 15:01:16. No dice qué contenía el extracto.

<a name="how"></a>
## Cómo funciona

1. **Instala.** El instalador instala Rashnova y su grabador en segundo plano.
2. **Elige un PIN.** El PIN lo comprueba el grabador, no la ventana de la aplicación.
3. **Antes de entregarlo:** **Repair Mode > Activate**, y luego tu PIN.
4. **Entrégalo.** Todo lo de "Qué hace" se escribe en un registro sellado.
5. **Al recuperarlo:** **Deactivate**, y luego tu PIN. Recibes un veredicto, un informe y la comprobación de la cadena.

El grabador funciona como un servicio de Windows, así que sigue grabando aunque nadie abra la ventana de
Rashnova, y vuelve a arrancar solo después de un reinicio.

**Cada sesión termina con uno de cuatro veredictos:**

| Veredicto | Significa |
| --- | --- |
| **Quiet** | El registro se verifica, está completo y no ocurrió nada de importancia alta. |
| **Notable** | Al menos un evento alto (high) o crítico (critical): conviene leerlo. |
| **Compromised** | El grabador de Rashnova se detuvo mientras Windows seguía funcionando, o el registro muestra una interferencia, así que no puede responder por toda la sesión. Un reinicio, un apagado o la suspensión se muestran con su duración y no cuentan en contra de la sesión. |
| **Chain broken** | El registro no se verifica. Se sigue mostrando todo, marcado como no verificado. |

<a name="download"></a>
## Descarga e instalación

| Archivo | Para qué |
| --- | --- |
| **`Rashnova-1.2.0.msi`** | Para todos. Instala Rashnova con su propia copia de .NET 10, así que no hace falta instalar nada antes. |
| `SHA256SUMS.txt` | El SHA-256 de cada archivo, para comprobar tu descarga. |

1. Descarga `Rashnova-1.2.0.msi` de la [última versión](https://github.com/sathvik-zoldyck/rashnova/releases/latest). Si tu navegador dice que el archivo no se descarga con frecuencia, elige **Keep** (los pasos para cada navegador están en los [límites conocidos](KNOWN_LIMITS.md)).
2. **Comprueba el archivo** (recomendado). En PowerShell:
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-1.2.0.msi"
   ```
   El hash debe coincidir exactamente con el de `SHA256SUMS.txt` y el de las notas de versión.
3. Ejecútalo. Windows SmartScreen muestra **"Windows protected your PC"** con un editor desconocido, porque el
   instalador aún no está firmado digitalmente (consulta los [límites conocidos](KNOWN_LIMITS.md)). Elige
   **More info** y después **Run anyway**.
4. Acepta los [términos de licencia](https://www.alcyonesecure.com/terms), instala y abre Rashnova.
5. Elige un PIN y decide si mantienes la grabación solo en sesiones (la opción predeterminada) o activas la
   grabación continua.


> [!IMPORTANT]
> Un PIN olvidado no se puede recuperar, ni por nosotros ni por nadie. Anótalo en un lugar seguro.
> Desactivar la grabación continua nunca necesita el PIN.


**¿Vienes de 1.1.0?** Instala 1.2.0 encima; tu registro, tu PIN y tus ajustes se conservan. **¿Vienes de BlackBox 1.0.1?** Rashnova es el nuevo nombre de BlackBox. Descarga e instala 1.2.0.

<a name="requirements"></a>
## Requisitos del sistema

- Windows 10 o Windows 11, 64 bits (probado en Windows 10)
- Nada más: Rashnova trae su propia copia de Microsoft .NET 10
- Permiso de administrador para instalar, porque el grabador funciona como un servicio de Windows

<a name="privacy"></a>
## Privacidad

- **Solo local.** El registro se escribe y se guarda en tu ordenador. En esta versión no hay cuenta ni nube, y Rashnova no
  envía datos de uso.
- **Dos pequeñas solicitudes,** ninguna con nada de tu registro: una comprobación diaria en alcyonesecure.com de si hay
  una versión nueva y, durante una Repair session, una comprobación de la hora con el servidor de hora de Microsoft.
- **Quién puede leer el registro.** La cuenta de Windows que eligió el PIN y los administradores del ordenador. La
  segunda copia está cifrada, y Rashnova solo la abre después de comprobar tu PIN. Los administradores del ordenador
  pueden leerla igualmente.
- **Avisa a quienes usan tu PC.** La grabación continua cubre todo el ordenador, incluidas las personas que nunca
  abren Rashnova.
- **Un ajuste de Windows, dicho con claridad.** Durante una sesión de Repair o Handover, Rashnova activa el registro de
  scripts de PowerShell de Windows y lo deja como estaba al terminar la sesión. Nunca desactiva un ajuste que otra persona activó.

<a name="limits"></a>
## Límites conocidos

Publicamos lo que Rashnova no hace, para que decidas con los hechos. Lo más importante:

- **No se puede registrar nada mientras el ordenador está apagado, en suspensión o reiniciándose.** La sesión sigue,
  y el informe muestra cada interrupción y su duración.
- **Los administradores pueden leer el registro.** Ningún programa puede ocultar sus archivos a un administrador de Windows.
- **El instalador aún no está firmado digitalmente,** así que tu navegador y Windows SmartScreen pueden avisar antes de ejecutarlo.
- **El bloqueo de almacenamiento USB detiene las unidades USB, no todas las formas de mover archivos.** No se bloquean los
  teléfonos, las ranuras SD integradas en el ordenador ni las unidades de red, y una unidad ya conectada sigue funcionando
  hasta que se desconecta.

La lista completa, con el motivo de cada uno y lo previsto (en inglés): **[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**.

<a name="updates"></a>
## Actualizaciones

Una vez al día Rashnova comprueba en alcyonesecure.com si hay una versión nueva y te avisa. La descargas e instalas
tú; tu registro, tu PIN y tus ajustes se conservan. Cada versión se publica aquí con sus notas y su SHA-256. Consulta el
[registro de cambios](CHANGELOG.md).

<a name="support"></a>
## Ayuda y seguridad

- **Ayuda:** consulta [SUPPORT.md](SUPPORT.md) o escribe a **support@alcyonesecure.com**.
- **Errores:** [abre un issue](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose). Nunca publiques tu
  registro, nombres de archivos ni nada personal en un issue.
- **Vulnerabilidades de seguridad:** no abras un issue público. Sigue [SECURITY.md](SECURITY.md).

<a name="licence"></a>
## Licencia

Rashnova es software propietario, gratuito para usar en dispositivos que te pertenecen o que estás autorizado a
supervisar. Consulta [LICENSE](LICENSE) y los [términos](https://www.alcyonesecure.com/terms) (en inglés; son los que
valen). Los documentos e imágenes de este repositorio son © Alcyone Secure.

---

<div align="center">

<img src="assets/rashnova-icon.png" alt="Rashnova" width="72">

**Alcyone Secure** · Hecho en Bengaluru, India · [alcyonesecure.com](https://www.alcyonesecure.com)

*La seguridad no es solo prevención. La seguridad es rendición de cuentas.*

</div>
