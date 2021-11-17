## Cloudflare Workers Sites

Perf is done by `npx autocannon [URL]`.

```
Running 10s test @ https://perf-cloudflare-workers-sites-vs-cloudflare-pages.xxx.workers.dev
10 connections

┌─────────┬───────┬───────┬───────┬───────┬──────────┬──────────┬─────────┐
│ Stat    │ 2.5%  │ 50%   │ 97.5% │ 99%   │ Avg      │ Stdev    │ Max     │
├─────────┼───────┼───────┼───────┼───────┼──────────┼──────────┼─────────┤
│ Latency │ 26 ms │ 33 ms │ 57 ms │ 71 ms │ 39.08 ms │ 59.56 ms │ 1141 ms │
└─────────┴───────┴───────┴───────┴───────┴──────────┴──────────┴─────────┘
┌───────────┬─────────┬─────────┬────────┬────────┬────────┬────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%    │ 97.5%  │ Avg    │ Stdev  │ Min     │
├───────────┼─────────┼─────────┼────────┼────────┼────────┼────────┼─────────┤
│ Req/Sec   │ 20      │ 20      │ 277    │ 291    │ 252.2  │ 77.69  │ 20      │
├───────────┼─────────┼─────────┼────────┼────────┼────────┼────────┼─────────┤
│ Bytes/Sec │ 43.8 kB │ 43.8 kB │ 607 kB │ 637 kB │ 552 kB │ 170 kB │ 43.8 kB │
└───────────┴─────────┴─────────┴────────┴────────┴────────┴────────┴─────────┘

Req/Bytes counts sampled once per second.

3k requests in 10.05s, 5.52 MB read
```

## Cloudflare Pages

```
Running 10s test @ https://perf-cloudflare-workers-sites-vs-cloudflare-pages.pages.dev/
10 connections

┌─────────┬───────┬───────┬───────┬───────┬──────────┬──────────┬────────┐
│ Stat    │ 2.5%  │ 50%   │ 97.5% │ 99%   │ Avg      │ Stdev    │ Max    │
├─────────┼───────┼───────┼───────┼───────┼──────────┼──────────┼────────┤
│ Latency │ 24 ms │ 32 ms │ 58 ms │ 78 ms │ 35.24 ms │ 20.78 ms │ 664 ms │
└─────────┴───────┴───────┴───────┴───────┴──────────┴──────────┴────────┘
┌───────────┬────────┬────────┬────────┬────────┬────────┬─────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg    │ Stdev   │ Min    │
├───────────┼────────┼────────┼────────┼────────┼────────┼─────────┼────────┤
│ Req/Sec   │ 234    │ 234    │ 284    │ 297    │ 278.8  │ 16.29   │ 234    │
├───────────┼────────┼────────┼────────┼────────┼────────┼─────────┼────────┤
│ Bytes/Sec │ 494 kB │ 494 kB │ 600 kB │ 627 kB │ 588 kB │ 34.4 kB │ 494 kB │
└───────────┴────────┴────────┴────────┴────────┴────────┴─────────┴────────┘

Req/Bytes counts sampled once per second.

3k requests in 10.04s, 5.88 MB read
```
