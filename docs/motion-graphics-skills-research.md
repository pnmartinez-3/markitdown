# Skills, subagentes, plugins y MCP para motion graphics, edición de video, Photoshop y diseño

Investigación del 14 de octubre de 2026.

- **Cómo se verificó:** los repos se confirmaron con la búsqueda de GitHub o leyendo su README.
- **Estrellas (★):** son una foto de ese día. Muchos repos se crearon en 2026 con contadores muy altos; tómalos como señal de popularidad, no de calidad.
- **Etiquetas:** *[web]* = solo se confirmó en documentación o buscadores; *[sin verificar]* = no se pudo confirmar.

> **Antes de instalar:** lee el SKILL.md o el código de cada repo. Muchos llaman a APIs de pago (ElevenLabs, Runway, Gemini, MuAPI, Atlas Cloud, Replicate, fal).

---

## 0. Ya instalado en este repo: Barty-Bart/motion-graphics

Ruta: `.claude/skills/`. Origen: https://github.com/Barty-Bart/motion-graphics, commit `3d83d98`, licencia MIT (671★).

| Skill | Qué hace |
|---|---|
| `motion-broll` | Toma un video y su transcripción y genera B-roll de motion graphics sincronizado con las palabras. |
| `object-separation` | Separa a una persona, producto o mano del fondo, en local con SAM 2 (rotoscopia). |
| `explainer-high-energy` | Promo de 12–20 s con tipografía cinética sincronizada al beat. |
| `explainer-default` | Demo de producto de 45–90 s que reconstruye la UI del producto. |
| `explainer-engaging` | Explainer de 10–30 s en una sola toma, siguiendo un elemento que recorre el flujo del producto. |
| `sound-effects` | Pase de sonido con SFX CC0 en el beat, mezclado a −16 LUFS y medido. |

**Requisitos:**
- `motion-broll` y los tres `explainer-*`: Node, Python 3, ffmpeg y Playwright/Chromium.
- `object-separation`: torch y transformers.
- `sound-effects`: librosa.

---

## 1. Recomendaciones principales (por dónde empezar)

| Necesidad | Instalar |
|---|---|
| Video programático con React | `npx skills add remotion-dev/skills` (oficial, 5.1k★) |
| HTML/GSAP a video | `claude plugin marketplace add heygen-com/hyperframes`, luego `claude plugin install hyperframes@hyperframes` (63k★) |
| Paquetes de motion design (TikTok, YouTube, ads, kinetic type, lower thirds, Manim, WebGL) | `npx skills add iart-ai/motion-skills` (810★) |
| GSAP correcto | `npx skills add greensock/gsap-skills` (oficial, 16k★) |
| Edición de video con agentes | browser-use/video-use (29k★), calesthio/OpenMontage (68k★) |
| Photoshop, Illustrator, Premiere, Firefly | Plugin oficial `adobe-for-creativity@claude-plugins-official` (ya conectado en esta sesión) |
| Photoshop local | `mikechambers/adb-mcp` (724★) o `npx -y @alisaitteke/photoshop-mcp` (642★, ~118 herramientas) |
| DaVinci Resolve | samuelgursky/davinci-resolve-mcp (3.5k★) |
| After Effects | Dakkshin/after-effects-mcp (742★) |
| Premiere Pro | hetpatel-11/Adobe_Premiere_Pro_MCP (690★) |
| Blender / 3D | ahujasid/mcp-for-blender (31k★, antes blender-mcp) |
| Voz, SFX y música | `npx skills add elevenlabs/skills` y elevenlabs/elevenlabs-mcp |
| Figma | `claude plugin install figma@claude-plugins-official` o GLips/Figma-Context-MCP (16k★) |
| Generación de imagen, video y 3D | Higgsfield MCP (ya conectado en esta sesión): `claude mcp add --transport http higgsfield https://mcp.higgsfield.ai/mcp` |

---

## 2. Motion graphics y video programático

### Remotion
- **remotion-dev/skills** — oficial, 12 skills (best-practices, create, render, captions, maps, studio, multimedia…). `npx skills add remotion-dev/skills`
- **@remotion/mcp** — solo busca en la documentación, no renderiza. `npx @remotion/mcp@latest`
- **Vincentwei1021/video-shotcraft** — videos de producto cinematográficos con 152 recetas de plano (11.9k★).
- **Vincentwei1021/anything2explainer** — explainer narrado con TTS y subtítulos (2.5k★).
- **Vincentwei1021/video-talkcraft** — explainers sincronizados con voz en off y tipografía cinética (1.6k★).
- **digitalsamba/claude-code-video-toolkit** — del concepto al MP4: guion, TTS, música y render (2.2k★).
- **gyoridavid/short-video-maker** — MCP para TikTok, Reels y Shorts (1.4k★).
- **haidrrrry/claude-remotion-skill** — motion, B-roll, captions y sonido (424★).
- **hassancs91/claude-youtube-editor** — talking head → corte → visuales → thumbnail → subida a YouTube (331★).

### HyperFrames (HeyGen)
- **heygen-com/hyperframes** — unos 20 skills: `/motion-graphics`, `/faceless-explainer`, `/embedded-captions`, `/talking-head-recut`, `/music-to-video`, `/remotion-to-hyperframes`.
- **latent-spaces/brag** — video de lanzamiento de un proyecto (15.9k★).
- **nateherkai/herk-edit-kit** — 15 skills, cortes guiados por transcripción y 406 tarjetas de motion (1.4k★).
- **nexu-io/html-video** — HTML a MP4 con 21 plantillas (4.7k★).
- **Tejashmakwana/motionmaxxing** — pule videos hechos por IA (452★).
- **Sunwood-ai-labs/hyperframes-motion-reel-skill** — showreel sincronizado al beat (128★).

### Manim y Motion Canvas
- **adithya-s-k/manim_skill** — animaciones estilo 3Blue1Brown (1.2k★).
- **Yusuke710/manim-skill** (171★).
- **shuyicc/MathLens** — explainer de matemáticas con Manim (358★).
- **AmitSubhash/3brown1blue** (37★).
- **abhiemj/manim-mcp-server** — MCP.
- **mainkunalhu/motion-canvas-skill** — muy nuevo; no hay skill oficial de Motion Canvas.

### GSAP, Lottie, Rive y animación web
- **greensock/gsap-skills** — oficial (16k★).
- **iart-ai/motion-skills** (810★), **iart-ai/web-animation-skills** y **iart-ai/webgl-animation-skills**.
- **lemomo-ai/lemo-opuscar** — 43 estilos de cortometraje hechos con código (2.3k★).
- **Alisa0808/vox-director** — explainers estilo Vox (2.3k★).
- **alexgreensh/anidoodle** (909★), **cth9191/animate** (684★), **AThevon/genjutsu** (481★).
- **talknerdytome-labs/wiggle-claude-skill** — anima logos a Lottie.
- **ODU33104/rive-mcp** — crea y edita archivos `.riv`.
- **yangagent/whiteboard-animation-skill** — animación de pizarra.
- **dylantarre/animation-principles** — skills `filmmaker` y `video-motion-graphics`.
- **HeyRenan/showreel** — GIFs, MP4 y grabaciones de terminal verificados.
- **Skills oficiales de Anthropic:** `slack-gif-creator`, `algorithmic-art`. `/plugin install example-skills@anthropic-agent-skills`
- **Lista curada:** frankxai/awesome-motion-design-agent-skills.

---

## 3. Edición de video

### After Effects
- **Dakkshin/after-effects-mcp** (742★)
- **kumoproductions/mcp-aftereffects** (111★)
- **JUNKDOGE-JOE/after-effects-mcp** (82★)
- **solomondivyananth/aftereffects-mcp** (44★)
- **ishu86/after-effects-mcp** — más de 70 herramientas.
- **a-y-ibrahim/after-effects-mcp**

### Premiere Pro
- **hetpatel-11/Adobe_Premiere_Pro_MCP** (690★)
- **leancoderkavy/premiere-pro-mcp** (376★)
- **ayushozha/AdobePremiereProMCP** (121★)
- **tro2789/scout-premiere-mcp** — búsqueda por transcripción, cortes y exportación.
- **antipaster/Adobe-Premiere-Pro-MCP** — más de 170 herramientas.

### DaVinci Resolve
- **samuelgursky/davinci-resolve-mcp** (3.5k★)
- **barckley75/resolve-claude-mcp** (384★)
- **hiteshK03/davinci-resolve-mcp** — incluye Whisper.
- **apvlv/davinci-resolve-mcp** — Resolve y Fusion.
- **wassermanproductions/unofficial-davinci-mcp** — para la edición gratuita.

### Final Cut Pro
- **elliotttate/SpliceKit** (170★)
- **DareDev256/fcp-mcp-server** — en PyPI.
- **elliotttate/finalcutpro-mcp**
- **dreliq9/fcp-mcp**

### CapCut / Jianying
- **sun-guannan/VectCutAPI** (2.3k★)
- **renezander030/capcut-cli** — `npx skills add renezander030/capcut-cli`
- **mrbuslov/capcut-ai-editor** — quita pausas y añade subtítulos.
- **xuliang2024/cutcli-cookbook**
- **zenstory-ai/video-recap-skills** (572★)

### Editores abiertos controlables por agentes
- **jub0t/concat** (5.4k★)
- **0xsline/OpenChatCut** (2.4k★)
- **veedstudio/open-edit** (1.7k★)
- **pireel/pireel** (1.3k★)
- **JimLiu/baocut** (953★)
- **cartesiancs/cartcut** (812★)

### FFmpeg
- **KyaniteLabs/kinocut** y **KyaniteLabs/mcp-video**
- **video-creator/ffmpeg-mcp**
- **egoist/ffmpeg-mcp**
- **misbahsy/video-audio-mcp**
- **kevinwatt/ffmpeg-mcp-lite**
- **Kush36Agrawal/Video_Editor_MCP**
- **AH64-dll/OpenEdit**

### Subtítulos, recorte de silencios y shorts
- **6missedcalls/video-editing-skill** — jump cuts, captions estilo Hormozi y eliminación de silencios.
- **mutonby/openshorts** — 9:16 con seguimiento de cara y publicación.
- **KevTheAIGuy/clipping-agent**
- **Tofuswang/video-subtitle-skill**
- **omerfarukdemiral/video-subtitles**
- **soanseng/podcast-use**

### Entender video (que Claude "vea" el video)
- **jordanrendric/claude-video-vision** (1.4k★)
- **guimatheus92/mcp-video-analyzer**

### Generación y avatares
- **runwayml/skills** — `npx skills add runwayml/skills`
- **heygen-com/skills** — avatar, video, traducción y skill `video-edit`.
- **SamurAIGPT/Generative-Media-Skills**
- **inferen-sh/skills** *[sin verificar]*

### Publicación
- **postiz** — plugin oficial.
- Plugins de la comunidad: `upload-post` y `post-bridge`.

---

## 4. Photoshop, imagen y diseño gráfico

### Adobe (oficial)
- **adobe-for-creativity** (adobe/skills) — Photoshop, Lightroom, Illustrator, InDesign, Express, Firefly, Premiere y Acrobat. Quita fondos, vectoriza, hace expansión generativa, retoca, gestiona fuentes y PDF.
- **MCP integrado en Illustrator Beta** *[web]*.

### Photoshop (comunidad)
- **mikechambers/adb-mcp** — UXP; controla Photoshop, Premiere, InDesign, After Effects e Illustrator (724★).
- **alisaitteke/photoshop-mcp** — ExtendScript, unas 118 herramientas (642★).
- **loonghao/photoshop-python-api-mcp-server** — Windows. `uvx photoshop-mcp-server`
- **znznzna/photoshop-cli** — macOS.
- **editmamei/editmamei** — edición no generativa.
- **dcc-mcp/dcc-mcp-photoshop**
- **TheWhykiki/photoshop-comfyui-mcp-bridge**
- **attalla1/photopea-mcp-server** — Photopea, en el navegador.
- **SFKislev/Flue** — controla Photoshop, Premiere, Blender, InDesign y más por COM o AppleScript.

### Illustrator e InDesign
- **ie3jp/illustrator-mcp-server** — 63 herramientas.
- **krVatsal/illustrator-mcp**
- **spencerhhubert/illustrator-mcp-server**
- **chris-enea/indesign-mcp**

### GIMP, Krita y Affinity
- **maorcc/gimp-mcp** (258★)
- **libreearth/gimp-mcp**
- **nanayax3/krita-mcp**
- **cyyprezz/krita-codex-mcp**
- **sekharmalla/affinity-mcp-server**
- Conector oficial de Affinity *[web]*.

### Figma y Canva
- **figma/mcp-server-guide** — oficial.
- **GLips/Figma-Context-MCP** (16k★)
- **grab/cursor-talk-to-figma-mcp** — lee y modifica diseños (7k★).
- **canva-sdks/canva-skills** — oficial; redimensiona, crea en lote y revisa la marca.

### Skills oficiales de Anthropic
- `canvas-design`
- `theme-factory`
- `brand-guidelines`
- `frontend-design`
- `algorithmic-art`

### Generación de imagen con IA
- **ComfyUI:** Comfy-Org/comfy-mcp (oficial) y joenorton/comfyui-mcp-server.
- **Nano Banana / Gemini:** AgriciDaniel/banana-claude (1.1k★), zhongweili/nanobanana-mcp-server y kkoppenhaver/cc-nano-banana.
- **OpenAI GPT Image:** SureScaleAI/openai-gpt-image-mcp.
- **Replicate / Flux:** awkoy/replicate-flux-mcp.
- **fal:** luminarylane/fal-mcp-server.
- **Leonardo:** MCP oficial *[web]*.
- **Freepik:** el repo oficial ahora da 404.
- **MeiGen-AI-Design-MCP** — generación y edición de imagen con enrutado a ComfyUI.

### Utilidades de imagen
- **Quitar fondo:** holocode-ai/rembg-mcp (o la librería danielgatis/rembg).
- **ImageMagick:** ncipollo/magick-mcp.
- **Cloudinary:** plugin oficial.
- **Upscaling:** no hay un MCP dedicado de Real-ESRGAN. Usa Higgsfield, Adobe o Replicate.

### SVG y vector
- **svgnew/plugin**
- **neonwatty/logo-designer-skill**
- **leonmeerfeld/logo-vectorize**
- **alonw0/web-asset-generator**

### Thumbnails
- **Jakeschincariol/youtube-agent-skill** (1.4k★)
- **AgriciDaniel/claude-youtube**
- **oil-oil/oil-cover**
- **aabrole/claude-video-thumbnail-skill**
- **charlie947/social-media-skills**

---

## 5. Audio, sonido y música
- **elevenlabs/skills** — TTS, STT, SFX, música, dubbing y aislamiento de voz.
- **elevenlabs/elevenlabs-mcp**
- **Ableton:** ahujasid/ableton-mcp.
- **REAPER:** TwelveTake-Studios/reaper-mcp.
- **js713-lab/sonic-match-mcp** — música con licencia segura.
- **Plugins de la comunidad:** `phantom` (mezcla y master), `djclaude`, `composing-with-pytheory`, `voxflow`.

## 6. 3D
- **ahujasid/mcp-for-blender** (31k★)
- **elithril/blender-kiln** — del brief a un GLB validado.
- **scenario-labs/skills** — Blender, Maya y Unreal.
- **squall01337/mixamo-llm-mocap**
- **Plugins oficiales:** `unity` y `unreal-engine-skills-for-claude-code`.

---

## 7. Subagentes
Las colecciones de subagentes casi no tienen nada de video, audio o diseño gráfico. Lo más cercano:
- **VoltAgent/awesome-claude-code-subagents** — `ui-designer`, `design-bridge`, `content-marketer`.
- **wshobson/agents** — plugins `ui-design`, `meigen-ai-design`, `file-conversion` (imagen, audio y video) y `social-publishing`.
- **0xfurai/claude-code-subagents** — `css-expert` (animaciones).
- **lst97/claude-code-sub-agents** y **davepoon/buildwithclaude** — nada específico de medios.

El ecosistema creativo se distribuye como **skills, plugins y MCP**, no como subagentes. Si quieres un subagente, se puede escribir uno en `.claude/agents/` que use estos skills.

## 8. Directorios para seguir buscando
| Directorio | Cómo buscar o instalar |
|---|---|
| anthropics/claude-plugins-official | `/plugin` → `/plugin install <nombre>@claude-plugins-official` |
| anthropics/claude-plugins-community | `claude plugin marketplace add anthropics/claude-plugins-community` (unos 60 plugins de medios) |
| skills.sh (Vercel) | `npx skills find <término>` y `npx skills add <owner/repo>` |
| claudemarketplaces.com | Categoría "Video & Audio Editing" |
| zhuyansen/awesome-claude-video-skills | Unos 180 repos de video con nota de seguridad |
| wilwaldon/Claude-Code-Video-Toolkit | Lista curada |
| punkpeye/awesome-mcp-servers | Secciones Multimedia Process, Art & Culture y Gaming |
| travisvn, ComposioHQ y hesreallyhim (awesome-claude-*) | Listas curadas generales |
| glama.ai, mcp.so y smithery.ai | Índices de MCP (no se pudieron consultar desde el sandbox) |
