# Building a Dashboard UI with React, TypeScript, and MUI

## 1. Project Setup

- **Create the project:**  
  Use [Vite](https://vitejs.dev/) for fast React + TypeScript scaffolding.

  ```sh
  npm create vite@latest . -- --template react-ts
  npm install
  ```

- **Install MUI and dependencies:**
  ```sh
  npm install @mui/material @emotion/react @emotion/styled @mui/icons-material
  npm install @fontsource/roboto
  ```

## 2. Project Structure

Organize your project for scalability:

```
app/
  nool-ui/
    src/
      components/   # Reusable React components
      pages/        # Top-level pages (e.g., Dashboard)
      hooks/        # Custom React hooks
      ...
    public/
    package.json
    ...
```

## 3. Basic App Setup

- **Entry Point:**  
  In `src/app.tsx`, set up the React root and import MUI’s Roboto font:

  ```tsx
  import { StrictMode } from "react";
  import { createRoot } from "react-dom/client";
  import "./index.css";
  import App from "./components/App";
  import "@fontsource/roboto/300.css";
  import "@fontsource/roboto/400.css";
  import "@fontsource/roboto/500.css";
  import "@fontsource/roboto/700.css";

  createRoot(document.getElementById("root")!).render(
    <StrictMode>
      <App />
    </StrictMode>
  );
  ```

## 4. Using MUI Components

- **Import and use MUI components:**

  ```tsx
  import Button from "@mui/material/Button";

  function MyComponent() {
    return (
      <Button variant="contained" color="primary">
        Hello MUI
      </Button>
    );
  }
  ```

- **Explore the [MUI docs](https://mui.com/material-ui/getting-started/overview/)** for more components.

## 5. Building the Dashboard Layout

- **Create a `Dashboard` page in `src/pages/Dashboard.tsx`.**
- Use MUI components like `AppBar`, `Drawer`, `Box`, and `Grid` to build your layout.
- Example:

  ```tsx
  import { AppBar, Toolbar, Typography, Box, Grid, Paper } from "@mui/material";

  export default function Dashboard() {
    return (
      <>
        <AppBar position="static">
          <Toolbar>
            <Typography variant="h6">Dashboard</Typography>
          </Toolbar>
        </AppBar>
        <Box p={2}>
          <Grid container spacing={2}>
            <Grid item xs={12} md={6}>
              <Paper>Widget 1</Paper>
            </Grid>
            <Grid item xs={12} md={6}>
              <Paper>Widget 2</Paper>
            </Grid>
          </Grid>
        </Box>
      </>
    );
  }
  ```

## 6. Routing (Optional)

- Use [react-router](https://reactrouter.com/) for multi-page dashboards.
  ```sh
  npm install react-router-dom
  ```

## 7. Customization & Theming

- Customize your dashboard’s look with MUI’s [ThemeProvider](https://mui.com/material-ui/customization/theming/).
- Example:

  ```tsx
  import { ThemeProvider, createTheme } from "@mui/material/styles";

  const theme = createTheme({
    palette: {
      primary: { main: "#1976d2" },
    },
  });

  <ThemeProvider theme={theme}>
    <App />
  </ThemeProvider>;
  ```

## 8. Fetching Data

- Use React hooks (`useEffect`, `useState`) to fetch and display data in your widgets.
- For real projects, consider a data-fetching library like [React Query](https://tanstack.com/query/latest) or [SWR](https://swr.vercel.app/).

## 9. Next Steps

- Add more widgets, charts (try [Recharts](https://recharts.org/) or [Victory](https://formidable.com/open-source/victory/)), and interactivity.
- Organize components for reusability.
- Add tests and polish your UI!

---

## Resources

- [MUI Documentation](https://mui.com/material-ui/getting-started/overview/)
- [Vite Documentation](https://vitejs.dev/)
- [React Documentation](https://react.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
