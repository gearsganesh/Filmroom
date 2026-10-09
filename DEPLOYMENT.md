# Filmroom browser deployment

## Vercel project settings

- Git repository: `gearsganesh/Filmroom`
- Production branch: `main`
- Root Directory: repository root (`.`); do not set it to `apps/filmcraft-web`
- Framework Preset: Other
- Install Command: `true` (the committed `vercel.json` controls this)
- Build Command: `bash deploy/vercel-build.sh`
- Output Directory: `target/web/dist`
- Environment variables: none required by the build script

Import or redeploy only after the latest `main` commit containing `deploy/vercel-build.sh` is available. The build uses `cargo xtask web` and `wasm-bindgen-cli` 0.2.129. Check the build logs for the final static output step before assigning the public domain.
