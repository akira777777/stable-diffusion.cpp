# Simple local image page

A single page for text-to-image with models already on this machine. It uses the
`sd-server` HTTP API. The official Web UI is unchanged.

## Start

Build `sd-server` first. From the repository root:

**Windows (PowerShell)**

```powershell
.\start-server.bat --serve-html-path examples\simple-ui\index.html
```

**Linux/macOS**

```sh
sh ./start-server.sh --serve-html-path examples/simple-ui/index.html
```

Open <http://127.0.0.1:1234/> and keep the server window open.

The page has to be served by `sd-server`. Opening `index.html` from the file
manager does not reach the API.

## Use

1. Put weights in the `models/` category folders described in the
   [server README](../server/README.md#model-directories).
2. Choose an image recipe.
3. Select each required component. A slot with one matching file is selected
   for you. When a recipe lists VAE or TAE together, either file satisfies that
   requirement.
4. Click **Load model** and wait until the status says ready.
5. Enter a prompt and click **Generate**.

Video recipes are hidden. LoRA, reference images, inpainting, and video
generation stay on the official Web UI.
