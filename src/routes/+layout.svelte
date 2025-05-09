<script>
    import { injectAnalytics } from '@vercel/analytics';
    import "../app.css";
    
    let { children } = $props();
    injectAnalytics();

  </script>
  {@render children()}






