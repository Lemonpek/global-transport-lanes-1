# Global Transport Control Tower - Static Deployment Package

This folder is a ready-to-upload static web package.

## Upload Targets

### Vercel
1. Go to https://vercel.com/new
2. Import or drag-upload this package content.
3. If using CLI, deploy this folder as static output:
   ```bash
   vercel deploy --prod
   ```

### Netlify
1. Go to https://app.netlify.com/drop
2. Drag and drop this folder or the zip file.
3. Netlify will serve `index.html` and use `_redirects` for SPA fallback.

### Azure Static Web Apps
1. Create a Static Web App in Azure Portal.
2. Use `deploy-static-package.zip` as the static artifact if your deployment path supports artifact upload, or upload this folder through SWA CLI:
   ```bash
   swa deploy . --deployment-token <token>
   ```

### Cloudflare Pages
1. Create a Pages project.
2. Upload this folder through Direct Upload.
3. The `_routes.json` file enables SPA fallback behavior.

## Notes

- This is a client-side static app. No backend server is included.
- Azure OpenAI values are placeholders in the current build, not real secrets.
- Spot News will fall back to local demo content unless real API integration is added through a backend proxy.
