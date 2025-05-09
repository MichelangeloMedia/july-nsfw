<script>
    import { dev } from '$app/environment';
    import { injectAnalytics } from '@vercel/analytics';
    import "../app.css";

    let { children } = $props();
    injectAnalytics({ mode: dev ? 'development' : 'production' });

  </script>
  {@render children()}






