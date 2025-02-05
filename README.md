
#  MUI Theme Color Palette in the Project

This project uses **Material UI (MUI) with a custom theme** to ensure a consistent design. The theme is **globally provided** using `ThemeProvider`, making it accessible across the entire application.
The theme is defined in `theme.ts` file and includes custom colors for primary, secondary, error, warning, info, success, and grey.

Since the project is wrapped with **`ThemeProvider`**, you can use theme colors in any component **without manually passing the theme**.

> [!TIP]
> **Recommended Way (Good Practice)**

Always use `theme.palette` for styling components to maintain consistency and flexibility.

#### **Using the `sx` Prop (Recommended)**
```tsx
import { Box, Button } from "@mui/material";

const MyComponent = () => {
  return (
    <Box
      sx={{
        backgroundColor: "primary.main",
        color: "error.main",
      }}
    >
      <Button variant="contained" color="secondary.main">
         My button
      </Button>
    </Box>
  );
};

export default MyComponent;
```

---

> [!WARNING]
> **Avoid This (Bad Practice)**

Never use **hardcoded color values** in components.

Never use **inline style** in components.

```tsx
const MyComponent = () => {
  return (
    <div style={{ backgroundColor: "#1a57ad" }}>
      <button style={{ backgroundColor: "#394b59", color: "#ffffff" }}>
         My button
      </button>
    </div>
  );
};
```


#### **Why is this a bad approach?**
- **Inconsistent styling** – If the theme colors change, these components won’t update automatically.
- **Breaks maintainability** – Finding and updating colors across multiple files is inefficient.
- **Ignores Dark Mode Support** – Hardcoded colors won’t adjust when switching to a dark theme.

---

The `theme.ts` file contains custom colors: primary, secondary, error, warning, info, success, and grey.

### Theme Color Palette
<!--  LaTeX Color Package: https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX -->

<table>
  <tr>
    <th colspan="3">Primary Palette</th>
    <td></td>
    <th colspan="3">Secondary Palette</th>
  </tr>
  <tr>
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
    <th/> <!-- Vertical Divider -->
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
  </tr>
  <tr>
    <td>$${\text{primary.light} \; \rule{80px}{0px}}$$</td>
    <td >$${\color{#006db6} \rule{100px}{60px}}$$</td>
    <td><code>#006db6</code></td>
    <td></td>
    <td>$${\text{secondary.light} \; \rule{80px}{0px}}$$</td>
    <td>$${\color{#4a6278} \rule{100px}{60px}}$$</td>
    <td><code>#4a6278</code></td>
  </tr>
  <tr>
    <td>$${\text{primary.main} \; \rule{80px}{0px}}$$</td>
    <td >$${\color{#1a57ad} \rule{100px}{60px}}$$</td>
    <td><code>#1a57ad</code></td>
    <td></td>
    <td>$${\text{secondary.main} \; \rule{80px}{0px}}$$</td>
    <td>$${\color{#394b59} \rule{100px}{60px}}$$</td>
    <td><code>#394b59</code></td>
  </tr>
  <tr>
    <td>$${\text{primary.dark} \; \rule{80px}{0px}}$$</td>
    <td >$${\color{#222c67} \rule{100px}{60px}}$$</td>
    <td><code>#222c67</code></td>
    <td></td>
    <td>$${\text{secondary.dark} \; \rule{80px}{0px}}$$</td>
    <td>$${\color{#293642} \rule{100px}{60px}}$$</td>
    <td><code>#293642</code></td>
  </tr>
</table>

<table>
  <tr>
    <th colspan="3">Error Palette</th>
    <td></td>
    <th colspan="3">Warning Palette</th>
  </tr>
  <tr>
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
    <th/> <!-- Vertical Divider -->
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
  </tr>
  <tr>
    <td>$${\text{error.light} \; \rule{100px}{0px}}$$</td>
    <td >$${\color{#ef5350} \rule{100px}{60px}}$$</td>
    <td><code>#ef5350</code></td>
    <td></td>
    <td>$${\text{warning.light} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#ff9800} \rule{100px}{60px}}$$</td>
    <td><code>#ff9800</code></td>
  </tr>
  <tr>
    <td>$${\text{error.main} \; \rule{100px}{0px}}$$</td>
    <td >$${\color{#d70000} \rule{100px}{60px}}$$</td>
    <td><code>#d70000</code></td>
    <td></td>
    <td>$${\text{warning.main} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#ec850c} \rule{100px}{60px}}$$</td>
    <td><code>#ec850c</code></td>
  </tr>
  <tr>
    <td>$${\text{error.dark} \; \rule{100px}{0px}}$$</td>
    <td >$${\color{#c62828} \rule{100px}{60px}}$$</td>
    <td><code>#c62828</code></td>
    <td></td>
    <td>$${\text{warning.dark} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#db7700} \rule{100px}{60px}}$$</td>
    <td><code>#db7700</code></td>
  </tr>
</table>

<table>
  <tr>
    <th colspan="3">Info Palette</th>
    <td></td>
    <th colspan="3">Success Palette</th>
  </tr>
  <tr>
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
    <th/> <!-- Vertical Divider -->
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
  </tr>
  <tr>
    <td>$${\text{info.light} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#216dd4} \rule{100px}{60px}}$$</td>
    <td><code>#216dd4</code></td>
    <td></td>
    <td>$${\text{success.light} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#4caf50} \rule{100px}{60px}}$$</td>
    <td><code>#4caf50</code></td>
  </tr>
  <tr>
    <td>$${\text{info.main} \; \rule{100px}{0px}}$$</td>
    <td >$${\color{#215db0} \rule{100px}{60px}}$$</td>
    <td><code>#215db0</code></td>
    <td></td>
    <td>$${\text{success.main} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#1f9b00} \rule{100px}{60px}}$$</td>
    <td><code>#1f9b00</code></td>
  </tr>
  <tr>
    <td>$${\text{info.dark} \; \rule{100px}{0px}}$$</td>
    <td >$${\color{#14468c} \rule{100px}{60px}}$$</td>
    <td><code>#14468c</code></td>
    <td></td>
    <td>$${\text{success.dark} \; \rule{100px}{0px}}$$</td>
    <td>$${\color{#198200} \rule{100px}{60px}}$$</td>
    <td><code>#198200</code></td>
  </tr>
</table>

### White to Black Color Palette

<table>
  <tr>
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
    <td/>
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
    <td/>
    <th>Color Name</th>
    <th>Color Preview</th>
    <th>Hex Code</th>
  </tr>
  <tr>
    <td>grey.100</td>
    <td >$${\color{#FFFFFF} \rule{100px}{60px}}$$</td>
    <td><code>#FFFFFF</code></td>
    <td/>
    <td>grey.500</td>
    <td >$${\color{#828282} \rule{100px}{60px}}$$</td>
    <td><code>#828282</code></td>
    <td/>
    <td>grey.900</td>
    <td >$${\color{#282828} \rule{100px}{60px}}$$</td>
    <td><code>#282828</code></td>
  </tr>
  <tr>
    <td>grey.200</td>
    <td >$${\color{#F5F5F5} \rule{100px}{60px}}$$</td>
    <td><code>#F5F5F5</code></td>
    <td/>
    <td>grey.600</td>
    <td >$${\color{#666666} \rule{100px}{60px}}$$</td>
    <td><code>#666666</code></td>
    <td/>
    <td>grey.1000</td>
    <td >$${\color{#191919} \rule{100px}{60px}}$$</td>
    <td><code>#191919</code></td>
  </tr>
  <tr>
    <td>grey.300</td>
    <td >$${\color{#EBEBEB} \rule{100px}{60px}}$$</td>
    <td><code>#EBEBEB</code></td>
    <td/>
    <td>grey.700</td>
    <td >$${\color{#505050} \rule{100px}{60px}}$$</td>
    <td><code>#505050</code></td>
    <td/>
    <td>grey.1100</td>
    <td >$${\color{#000000} \rule{100px}{60px}}$$</td>
    <td><code>#000000</code></td>
  </tr>
  <tr>
    <td>grey.400</td>
    <td >$${\color{#DCDCDC} \rule{100px}{60px}}$$</td>
    <td><code>#DCDCDC</code></td>
    <td/>
    <td>grey.800</td>
    <td >$${\color{#3C3C3C} \rule{100px}{60px}}$$</td>
    <td><code>#3C3C3C</code></td>
    <td/>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>


