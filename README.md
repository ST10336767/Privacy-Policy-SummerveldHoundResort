# SummerVeld Hound Resort - Privacy Policy Website

This repository contains a static website hosting the privacy policy for the SummerVeld Hound Resort App, designed to be deployed on GitHub Pages or Azure.

## 📁 Project Structure

```
├── index.html              # Main HTML file with privacy policy content
├── styles.css              # CSS styling for professional appearance
├── .github/workflows/      # GitHub Actions for automated deployment
├── _config.yml            # Jekyll configuration for GitHub Pages
├── web.config             # Azure IIS configuration
├── azure-pipelines.yml    # Azure DevOps CI/CD pipeline
├── package.json           # Node.js dependencies and scripts
└── README.md             # This file
```

## 🚀 Deployment Options

### Option 1: GitHub Pages (Recommended - FREE!)

1. **Fork or clone this repository**
2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll to "Pages" section
   - Select "GitHub Actions" as source
   - The workflow will automatically deploy on push to main branch

3. **Your site will be available at**:
   ```
   https://ST10336767.github.io/Privacy-Policy-SummerveldHoundResort
   ```

4. **Custom domain (optional)**:
   - Add a `CNAME` file with your domain
   - Configure DNS to point to your GitHub Pages site

### Option 2: Azure Static Web Apps

1. **Create Azure Static Web App**:
   ```bash
   az staticwebapp create \
     --name "summerveld-privacy-policy" \
     --resource-group "your-resource-group" \
     --source "https://github.com/your-username/your-repo" \
     --location "Central US" \
     --branch "main" \
     --app-location "/" \
     --output-location "/"
   ```

2. **Deploy using Azure CLI**:
   ```bash
   az staticwebapp deploy \
     --name "summerveld-privacy-policy" \
     --resource-group "your-resource-group" \
     --source-location "." \
     --deployment-token "your-deployment-token"
   ```

### Option 3: Azure App Service

1. **Create App Service**:
   ```bash
   az webapp create \
     --name "summerveld-privacy-policy" \
     --resource-group "your-resource-group" \
     --plan "your-app-service-plan"
   ```

2. **Deploy using Azure CLI**:
   ```bash
   az webapp deployment source config-zip \
     --name "summerveld-privacy-policy" \
     --resource-group "your-resource-group" \
     --src "deployment.zip"
   ```

### Option 4: Azure DevOps Pipeline

1. **Set up Azure DevOps**:
   - Create a new pipeline
   - Connect to your repository
   - Use the provided `azure-pipelines.yml`

2. **Configure Variables**:
   - `azureServiceConnection`: Your Azure service connection
   - `appName`: Your Azure Web App name

## 🛠️ Local Development

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start local server**:
   ```bash
   npm start
   ```

3. **View website**: Open http://localhost:8080

## 📋 Features

- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Professional Styling**: Clean, modern design with gradient header
- **SEO Optimized**: Proper meta tags and semantic HTML
- **Security Headers**: Security-focused configuration
- **Print Friendly**: Optimized for printing
- **Accessibility**: Proper heading structure and semantic markup

## 🔧 Customization

### Updating Content
- Edit `index.html` to modify the privacy policy content
- Update the "Last Updated" date in the header section

### Styling Changes
- Modify `styles.css` to change colors, fonts, or layout
- The design uses CSS custom properties for easy theming

### Configuration
- Update `web.config` for IIS-specific settings
- Modify `azure-pipelines.yml` for CI/CD customization

## 🌐 Domain and SSL

### GitHub Pages
- **Free SSL**: GitHub Pages provides free SSL certificates
- **Custom Domain**: Add a `CNAME` file with your domain name
- **Automatic HTTPS**: Enabled by default on GitHub Pages

### Azure (if using Azure options)
1. **Add custom domain in Azure portal**
2. **Configure DNS records**:
   - CNAME record pointing to your Azure app
   - A record for apex domain (if needed)
3. **SSL Certificate**: Azure provides free SSL certificates for custom domains

## 📊 Monitoring and Analytics

Consider adding:
- **Azure Application Insights** for performance monitoring
- **Google Analytics** for usage statistics
- **Azure Monitor** for health checks

## 🔒 Security Considerations

The website includes:
- Security headers (X-Content-Type-Options, X-Frame-Options, etc.)
- HTTPS enforcement
- No sensitive data exposure
- Static content only (no server-side processing)

## 📞 Support

For questions about this privacy policy website:
- **Email**: keatonjones02@gmail.com
- **Phone**: 0845698466

## 📄 License

This project is licensed under the MIT License.

---

**Note**: This is a static website hosting a privacy policy. No user data is collected or processed by this website itself.
