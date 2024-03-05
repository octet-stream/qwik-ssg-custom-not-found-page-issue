# qwik-ssg-custom-not-found-page-issue

Reproduction for issue with cutom 404 page when ssg disabled

## Reproduction

1. Clone this repository
2. Install dependencies via `bun i`
3. Build the project `bun run build`
4. Start the app `bun run serve`
5. Open [http://localhost:3000/404](http://localhost:3000/404) and you'll see the default Qwik route error
6. Navigate to [http://localhost:3000/404.html](http://localhost:3000/404.html) and you'll see custom 404 error page, just like in developmen
7. Stop the app
8. Comment out the 18th line in `adapters/bun/vite.config.ts`
9. Build project again
10. Start the app again and repeat steps `5` and `6`. You'll see that 404 page is served for any unmatched route, as expected
