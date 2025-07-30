# BookBazaar Server Status

## Current Status: ✅ WORKING

### Servers Running:

1. **LibraryAPI (Backend)**: http://localhost:7110

   - Status: ✅ Running
   - Swagger UI: http://localhost:7110/swagger
   - Endpoints: `/api/Books/all`, `/api/Books`, etc.

2. **LibraryWeb (Frontend)**: http://localhost:5185
   - Status: ✅ Running
   - Browse Books: http://localhost:5185/Home/BrowseBooks

### Recent Fixes:

1. **CORS Configuration**: Updated to allow all origins for development
2. **HTTPS to HTTP**: Changed API to use HTTP instead of HTTPS to avoid SSL issues
3. **Port Configuration**: Ensured both servers run on correct ports
4. **Navbar Authentication**: Fixed JWT token parsing in `_Layout.cshtml`

### Key Files Modified:

- `LibraryAPI/Program.cs` - CORS and HTTPS redirection
- `LibraryAPI/Properties/launchSettings.json` - Port configuration
- `LibraryWeb/Program.cs` - API client base URL
- `LibraryWeb/Views/Shared/_Layout.cshtml` - Authentication logic

### How to Start Servers:

**Terminal 1 - API Server:**

```bash
cd LibraryAPI
dotnet run --urls "http://localhost:7110"
```

**Terminal 2 - Web Server:**

```bash
cd LibraryWeb
dotnet run
```

### Testing:

- ✅ API accessible via browser: http://localhost:7110/swagger
- ✅ Web app accessible: http://localhost:5185
- ✅ Browse Books button working: redirects to /Books/Index
- ✅ API calls from web app successful

### Debug Features:

- Press `Ctrl+Shift+D` in the web app to open debug panel
- Console logs available in browser developer tools
- API logs visible in LibraryAPI terminal

Last Updated: $(Get-Date)
