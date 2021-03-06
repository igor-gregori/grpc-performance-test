# Caso 1:
> gateway@1.0.0 loadtest:express:case:1
> npx autocannon -c 1 -a 1000 localhost:3000/express/read/low-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/express/read/low-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬────────┬──────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev  │ Max  │
├─────────┼──────┼──────┼───────┼──────┼─────────┼────────┼──────┤
│ Latency │ 1 ms │ 1 ms │ 2 ms  │ 2 ms │ 1.03 ms │ 0.3 ms │ 6 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴────────┴──────┘
┌───────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg    │ Stdev  │ Min    │
├───────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┤
│ Req/Sec   │ 283    │ 283    │ 283    │ 717    │ 500    │ 217    │ 283    │
├───────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┤
│ Bytes/Sec │ 436 kB │ 436 kB │ 436 kB │ 1.1 MB │ 770 kB │ 334 kB │ 436 kB │
└───────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 1.54 MB read

> gateway@1.0.0 loadtest:grpc:case:1
> npx autocannon -c 1 -a 1000 localhost:3000/grpc/read/low-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/grpc/read/low-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 0 ms │ 1 ms │ 2 ms  │ 2 ms │ 1.07 ms │ 2.12 ms │ 67 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg    │ Stdev  │ Min    │
├───────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┤
│ Req/Sec   │ 364    │ 364    │ 364    │ 636    │ 500    │ 136    │ 364    │
├───────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┤
│ Bytes/Sec │ 558 kB │ 558 kB │ 558 kB │ 975 kB │ 766 kB │ 208 kB │ 558 kB │
└───────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 1.53 MB read

# Caso 2:
> gateway@1.0.0 loadtest:express:case:2
> npx autocannon -c 1 -a 1000 localhost:3000/express/read/medium-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/express/read/medium-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬──────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max  │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼──────┤
│ Latency │ 1 ms │ 1 ms │ 2 ms  │ 2 ms │ 1.05 ms │ 0.37 ms │ 9 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴──────┘
┌───────────┬─────────┬─────────┬─────────┬─────────┬─────────┬────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%   │ Avg     │ Stdev  │ Min     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼────────┼─────────┤
│ Req/Sec   │ 350     │ 350     │ 350     │ 650     │ 500     │ 150    │ 350     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼────────┼─────────┤
│ Bytes/Sec │ 2.19 MB │ 2.19 MB │ 2.19 MB │ 4.07 MB │ 3.13 MB │ 940 kB │ 2.19 MB │
└───────────┴─────────┴─────────┴─────────┴─────────┴─────────┴────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 6.26 MB read

> gateway@1.0.0 loadtest:grpc:case:2
> npx autocannon -c 1 -a 1000 localhost:3000/grpc/read/medium-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/grpc/read/medium-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 1 ms │ 1 ms │ 2 ms  │ 2 ms │ 1.06 ms │ 0.44 ms │ 12 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬─────────┬─────────┬────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%   │ Avg     │ Stdev  │ Min     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼────────┼─────────┤
│ Req/Sec   │ 359     │ 359     │ 359     │ 641     │ 500     │ 141    │ 359     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼────────┼─────────┤
│ Bytes/Sec │ 2.29 MB │ 2.29 MB │ 2.29 MB │ 4.09 MB │ 3.19 MB │ 900 kB │ 2.29 MB │
└───────────┴─────────┴─────────┴─────────┴─────────┴─────────┴────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 6.38 MB read

# Caso 3:
> gateway@1.0.0 loadtest:express:case:3
> npx autocannon -c 1 -a 1000 localhost:3000/express/read/high-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/express/read/high-payload
1 connections

┌─────────┬──────┬──────┬───────┬───────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%   │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼───────┼─────────┼─────────┼───────┤
│ Latency │ 7 ms │ 8 ms │ 11 ms │ 13 ms │ 7.97 ms │ 1.08 ms │ 16 ms │
└─────────┴──────┴──────┴───────┴───────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬───────┬─────────┬────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%   │ 97.5%   │ Avg    │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼───────┼─────────┼────────┼─────────┼─────────┤
│ Req/Sec   │ 58      │ 58      │ 119   │ 121     │ 111.12 │ 19.13   │ 58      │
├───────────┼─────────┼─────────┼───────┼─────────┼────────┼─────────┼─────────┤
│ Bytes/Sec │ 14.1 MB │ 14.1 MB │ 29 MB │ 29.5 MB │ 27 MB  │ 4.66 MB │ 14.1 MB │
└───────────┴─────────┴─────────┴───────┴─────────┴────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 9.02s, 243 MB read

> gateway@1.0.0 loadtest:grpc:case:3
> npx autocannon -c 1 -a 1000 localhost:3000/grpc/read/high-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/grpc/read/high-payload
1 connections

┌─────────┬──────┬──────┬───────┬───────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%   │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼───────┼─────────┼─────────┼───────┤
│ Latency │ 9 ms │ 9 ms │ 15 ms │ 16 ms │ 10.1 ms │ 1.98 ms │ 40 ms │
└─────────┴──────┴──────┴───────┴───────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%   │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 68      │ 68      │ 94      │ 96      │ 90.91   │ 7.98    │ 68      │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 25.3 MB │ 25.3 MB │ 34.9 MB │ 35.7 MB │ 33.8 MB │ 2.96 MB │ 25.3 MB │
└───────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 11.01s, 372 MB read

# Caso 4:
> gateway@1.0.0 loadtest:express:case:4
> npx autocannon -c 10 -d 30 localhost:3000/express/read/low-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/express/read/low-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 4 ms │ 4 ms │ 7 ms  │ 8 ms │ 4.45 ms │ 0.96 ms │ 18 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬────────┬─────────┬────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%  │ Avg     │ Stdev  │ Min     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼────────┼─────────┤
│ Req/Sec   │ 1420    │ 1420    │ 2042    │ 2077   │ 1976.97 │ 163.07 │ 1420    │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼────────┼─────────┤
│ Bytes/Sec │ 2.19 MB │ 2.19 MB │ 3.15 MB │ 3.2 MB │ 3.04 MB │ 251 kB │ 2.19 MB │
└───────────┴─────────┴─────────┴─────────┴────────┴─────────┴────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 59297 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

59k requests in 30.01s, 91.3 MB read

> gateway@1.0.0 loadtest:grpc:case:4
> npx autocannon -c 10 -d 30 localhost:3000/grpc/read/low-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/grpc/read/low-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 3 ms │ 4 ms │ 7 ms  │ 7 ms │ 3.99 ms │ 0.87 ms │ 12 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬────────┬─────────┬────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%  │ Avg     │ Stdev  │ Min     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼────────┼─────────┤
│ Req/Sec   │ 1528    │ 1528    │ 2309    │ 2419   │ 2274.7  │ 158.82 │ 1528    │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼────────┼─────────┤
│ Bytes/Sec │ 2.34 MB │ 2.34 MB │ 3.54 MB │ 3.7 MB │ 3.48 MB │ 243 kB │ 2.34 MB │
└───────────┴─────────┴─────────┴─────────┴────────┴─────────┴────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 68220 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

68k requests in 30.01s, 105 MB read


# Caso 5:
> gateway@1.0.0 loadtest:express:case:5
> npx autocannon -c 10 -d 30 localhost:3000/express/read/medium-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/express/read/medium-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 5 ms │ 5 ms │ 7 ms  │ 9 ms │ 5.33 ms │ 0.77 ms │ 15 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬───────┬─────────┬────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5% │ Avg     │ Stdev  │ Min     │
├───────────┼─────────┼─────────┼─────────┼───────┼─────────┼────────┼─────────┤
│ Req/Sec   │ 1287    │ 1287    │ 1719    │ 1753  │ 1698.9  │ 85.47  │ 1287    │
├───────────┼─────────┼─────────┼─────────┼───────┼─────────┼────────┼─────────┤
│ Bytes/Sec │ 8.06 MB │ 8.06 MB │ 10.8 MB │ 11 MB │ 10.6 MB │ 535 kB │ 8.06 MB │
└───────────┴─────────┴─────────┴─────────┴───────┴─────────┴────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 50967 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

51k requests in 30.01s, 319 MB read

> gateway@1.0.0 loadtest:grpc:case:5
> npx autocannon -c 10 -d 30 localhost:3000/grpc/read/medium-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/grpc/read/medium-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg    │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼────────┼─────────┼───────┤
│ Latency │ 4 ms │ 5 ms │ 8 ms  │ 9 ms │ 5.3 ms │ 0.96 ms │ 14 ms │
└─────────┴──────┴──────┴───────┴──────┴────────┴─────────┴───────┘
┌───────────┬────────┬────────┬─────────┬─────────┬─────────┬────────┬─────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%     │ 97.5%   │ Avg     │ Stdev  │ Min     │
├───────────┼────────┼────────┼─────────┼─────────┼─────────┼────────┼─────────┤
│ Req/Sec   │ 1534   │ 1534   │ 1770    │ 1806    │ 1758    │ 46.86  │ 1534    │
├───────────┼────────┼────────┼─────────┼─────────┼─────────┼────────┼─────────┤
│ Bytes/Sec │ 9.8 MB │ 9.8 MB │ 11.3 MB │ 11.5 MB │ 11.2 MB │ 299 kB │ 9.79 MB │
└───────────┴────────┴────────┴─────────┴─────────┴─────────┴────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 52740 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

53k requests in 30.01s, 337 MB read

# Caso 6:
> gateway@1.0.0 loadtest:express:case:6
> npx autocannon -c 10 -d 30 localhost:3000/express/read/high-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/express/read/high-payload
10 connections

┌─────────┬───────┬───────┬───────┬───────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5%  │ 50%   │ 97.5% │ 99%   │ Avg     │ Stdev   │ Max   │
├─────────┼───────┼───────┼───────┼───────┼─────────┼─────────┼───────┤
│ Latency │ 50 ms │ 53 ms │ 62 ms │ 66 ms │ 53.7 ms │ 3.54 ms │ 86 ms │
└─────────┴───────┴───────┴───────┴───────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%   │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 165     │ 165     │ 186     │ 191     │ 184.34  │ 5.47    │ 165     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 40.2 MB │ 40.2 MB │ 45.3 MB │ 46.5 MB │ 44.9 MB │ 1.33 MB │ 40.2 MB │
└───────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 5530  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

6k requests in 30.02s, 1.35 GB read

> gateway@1.0.0 loadtest:grpc:case:6
> npx autocannon -c 10 -d 30 localhost:3000/grpc/read/high-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/grpc/read/high-payload
10 connections

┌─────────┬───────┬───────┬────────┬────────┬──────────┬──────────┬────────┐
│ Stat    │ 2.5%  │ 50%   │ 97.5%  │ 99%    │ Avg      │ Stdev    │ Max    │
├─────────┼───────┼───────┼────────┼────────┼──────────┼──────────┼────────┤
│ Latency │ 70 ms │ 91 ms │ 120 ms │ 122 ms │ 93.15 ms │ 15.14 ms │ 214 ms │
└─────────┴───────┴───────┴────────┴────────┴──────────┴──────────┴────────┘
┌───────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%   │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 90      │ 90      │ 107     │ 110     │ 106.7   │ 4.07    │ 90      │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 33.4 MB │ 33.4 MB │ 39.8 MB │ 40.9 MB │ 39.6 MB │ 1.52 MB │ 33.4 MB │
└───────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 3201  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

3k requests in 30.02s, 1.19 GB read

# Caso 7:
> gateway@1.0.0 loadtest:express:case:7
> npx autocannon -c 1 -a 1000 localhost:3000/express/write/low-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/express/write/low-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬──────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max  │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼──────┤
│ Latency │ 0 ms │ 1 ms │ 1 ms  │ 2 ms │ 0.89 ms │ 0.49 ms │ 9 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴──────┘
┌───────────┬─────────┬─────────┬─────────┬────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%  │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 223     │ 223     │ 223     │ 777    │ 500     │ 277     │ 223     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 32.3 kB │ 32.3 kB │ 32.3 kB │ 113 kB │ 72.5 kB │ 40.2 kB │ 32.3 kB │
└───────────┴─────────┴─────────┴─────────┴────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 145 kB read

> gateway@1.0.0 loadtest:grpc:case:7
> npx autocannon -c 1 -a 1000 localhost:3000/grpc/write/low-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/grpc/write/low-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 0 ms │ 1 ms │ 1 ms  │ 2 ms │ 0.62 ms │ 0.61 ms │ 10 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%  │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 151     │ 151     │ 151     │ 849    │ 500     │ 349     │ 151     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 21.9 kB │ 21.9 kB │ 21.9 kB │ 123 kB │ 72.5 kB │ 50.6 kB │ 21.9 kB │
└───────────┴─────────┴─────────┴─────────┴────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.02s, 145 kB read

# Caso 8:
> gateway@1.0.0 loadtest:express:case:8
> npx autocannon -c 1 -a 1000 localhost:3000/express/write/medium-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/express/write/medium-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬────────┬─────────┬──────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg    │ Stdev   │ Max  │
├─────────┼──────┼──────┼───────┼──────┼────────┼─────────┼──────┤
│ Latency │ 0 ms │ 1 ms │ 1 ms  │ 2 ms │ 0.7 ms │ 0.58 ms │ 8 ms │
└─────────┴──────┴──────┴───────┴──────┴────────┴─────────┴──────┘
┌───────────┬─────────┬─────────┬─────────┬────────┬─────────┬───────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%  │ Avg     │ Stdev │ Min     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼───────┼─────────┤
│ Req/Sec   │ 155     │ 155     │ 155     │ 845    │ 500     │ 345   │ 155     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼───────┼─────────┤
│ Bytes/Sec │ 22.5 kB │ 22.5 kB │ 22.5 kB │ 123 kB │ 72.5 kB │ 50 kB │ 22.5 kB │
└───────────┴─────────┴─────────┴─────────┴────────┴─────────┴───────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 145 kB read

> gateway@1.0.0 loadtest:grpc:case:8
> npx autocannon -c 1 -a 1000 localhost:3000/grpc/write/medium-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/grpc/write/medium-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 0 ms │ 1 ms │ 1 ms  │ 1 ms │ 0.54 ms │ 0.61 ms │ 10 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%  │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 119     │ 119     │ 119     │ 881    │ 500     │ 381     │ 119     │
├───────────┼─────────┼─────────┼─────────┼────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 17.3 kB │ 17.3 kB │ 17.3 kB │ 128 kB │ 72.5 kB │ 55.3 kB │ 17.3 kB │
└───────────┴─────────┴─────────┴─────────┴────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 2.01s, 145 kB read

# Caso 9:
> gateway@1.0.0 loadtest:express:case:9
> npx autocannon -c 1 -a 1000 localhost:3000/express/write/high-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/express/write/high-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 2 ms │ 2 ms │ 6 ms  │ 7 ms │ 2.36 ms │ 0.98 ms │ 10 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%     │ 97.5%   │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 24      │ 24      │ 316     │ 330     │ 250     │ 130.61  │ 24      │
├───────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 3.48 kB │ 3.48 kB │ 45.8 kB │ 47.9 kB │ 36.3 kB │ 18.9 kB │ 3.48 kB │
└───────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 4.01s, 145 kB read

> gateway@1.0.0 loadtest:grpc:case:9
> npx autocannon -c 1 -a 1000 localhost:3000/grpc/write/high-payload --renderStatusCodes

Running 1000 requests test @ http://localhost:3000/grpc/write/high-payload
1 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 5 ms │ 6 ms │ 8 ms  │ 9 ms │ 6.19 ms │ 1.17 ms │ 26 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬─────────┬─────────┬───────┬─────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%   │ 97.5%   │ Avg     │ Stdev   │ Min     │
├───────────┼─────────┼─────────┼───────┼─────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 103     │ 103     │ 152   │ 156     │ 142.86  │ 17.88   │ 103     │
├───────────┼─────────┼─────────┼───────┼─────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 14.9 kB │ 14.9 kB │ 22 kB │ 22.6 kB │ 20.7 kB │ 2.59 kB │ 14.9 kB │
└───────────┴─────────┴─────────┴───────┴─────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 1000  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

1k requests in 7.02s, 145 kB read

# Caso 10:
> gateway@1.0.0 loadtest:express:case:10
> npx autocannon -c 10 -d 30 localhost:3000/express/write/low-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/express/write/low-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev  │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼────────┼───────┤
│ Latency │ 3 ms │ 4 ms │ 5 ms  │ 7 ms │ 4.14 ms │ 0.6 ms │ 14 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴────────┴───────┘
┌───────────┬────────┬────────┬────────┬────────┬────────┬─────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg    │ Stdev   │ Min    │
├───────────┼────────┼────────┼────────┼────────┼────────┼─────────┼────────┤
│ Req/Sec   │ 1805   │ 1805   │ 2183   │ 2287   │ 2177.6 │ 81.82   │ 1805   │
├───────────┼────────┼────────┼────────┼────────┼────────┼─────────┼────────┤
│ Bytes/Sec │ 262 kB │ 262 kB │ 317 kB │ 332 kB │ 316 kB │ 11.9 kB │ 262 kB │
└───────────┴────────┴────────┴────────┴────────┴────────┴─────────┴────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 65314 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

65k requests in 30.01s, 9.47 MB read

> gateway@1.0.0 loadtest:grpc:case:10
> npx autocannon -c 10 -d 30 localhost:3000/grpc/write/low-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/grpc/write/low-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg    │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼────────┼─────────┼───────┤
│ Latency │ 3 ms │ 3 ms │ 5 ms  │ 7 ms │ 3.2 ms │ 0.68 ms │ 12 ms │
└─────────┴──────┴──────┴───────┴──────┴────────┴─────────┴───────┘
┌───────────┬────────┬────────┬────────┬────────┬─────────┬─────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg     │ Stdev   │ Min    │
├───────────┼────────┼────────┼────────┼────────┼─────────┼─────────┼────────┤
│ Req/Sec   │ 2295   │ 2295   │ 2713   │ 2843   │ 2709.14 │ 96.03   │ 2294   │
├───────────┼────────┼────────┼────────┼────────┼─────────┼─────────┼────────┤
│ Bytes/Sec │ 333 kB │ 333 kB │ 393 kB │ 412 kB │ 393 kB  │ 13.9 kB │ 333 kB │
└───────────┴────────┴────────┴────────┴────────┴─────────┴─────────┴────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 81254 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

81k requests in 30.01s, 11.8 MB read

# Caso 11:
> gateway@1.0.0 loadtest:express:case:11
> npx autocannon -c 10 -d 30 localhost:3000/express/write/medium-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/express/write/medium-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬─────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg     │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼─────────┼─────────┼───────┤
│ Latency │ 4 ms │ 4 ms │ 6 ms  │ 7 ms │ 4.21 ms │ 0.67 ms │ 21 ms │
└─────────┴──────┴──────┴───────┴──────┴─────────┴─────────┴───────┘
┌───────────┬────────┬────────┬────────┬────────┬─────────┬─────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg     │ Stdev   │ Min    │
├───────────┼────────┼────────┼────────┼────────┼─────────┼─────────┼────────┤
│ Req/Sec   │ 1940   │ 1940   │ 2127   │ 2199   │ 2115.44 │ 59.62   │ 1940   │
├───────────┼────────┼────────┼────────┼────────┼─────────┼─────────┼────────┤
│ Bytes/Sec │ 281 kB │ 281 kB │ 308 kB │ 319 kB │ 307 kB  │ 8.61 kB │ 281 kB │
└───────────┴────────┴────────┴────────┴────────┴─────────┴─────────┴────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 63448 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

63k requests in 30.01s, 9.2 MB read

> gateway@1.0.0 loadtest:grpc:case:11
> npx autocannon -c 10 -d 30 localhost:3000/grpc/write/medium-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/grpc/write/medium-payload
10 connections

┌─────────┬──────┬──────┬───────┬──────┬────────┬─────────┬───────┐
│ Stat    │ 2.5% │ 50%  │ 97.5% │ 99%  │ Avg    │ Stdev   │ Max   │
├─────────┼──────┼──────┼───────┼──────┼────────┼─────────┼───────┤
│ Latency │ 3 ms │ 3 ms │ 6 ms  │ 6 ms │ 3.5 ms │ 0.88 ms │ 17 ms │
└─────────┴──────┴──────┴───────┴──────┴────────┴─────────┴───────┘
┌───────────┬────────┬────────┬────────┬────────┬─────────┬─────────┬────────┐
│ Stat      │ 1%     │ 2.5%   │ 50%    │ 97.5%  │ Avg     │ Stdev   │ Min    │
├───────────┼────────┼────────┼────────┼────────┼─────────┼─────────┼────────┤
│ Req/Sec   │ 1887   │ 1887   │ 2467   │ 2559   │ 2454.81 │ 116.08  │ 1887   │
├───────────┼────────┼────────┼────────┼────────┼─────────┼─────────┼────────┤
│ Bytes/Sec │ 274 kB │ 274 kB │ 358 kB │ 371 kB │ 356 kB  │ 16.8 kB │ 274 kB │
└───────────┴────────┴────────┴────────┴────────┴─────────┴─────────┴────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 73628 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

74k requests in 30.02s, 10.7 MB read

# Caso 12:
> gateway@1.0.0 loadtest:express:case:12
> npx autocannon -c 10 -d 30 localhost:3000/express/write/high-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/express/write/high-payload
10 connections

┌─────────┬───────┬───────┬───────┬───────┬──────────┬─────────┬───────┐
│ Stat    │ 2.5%  │ 50%   │ 97.5% │ 99%   │ Avg      │ Stdev   │ Max   │
├─────────┼───────┼───────┼───────┼───────┼──────────┼─────────┼───────┤
│ Latency │ 19 ms │ 22 ms │ 31 ms │ 33 ms │ 22.22 ms │ 2.47 ms │ 43 ms │
└─────────┴───────┴───────┴───────┴───────┴──────────┴─────────┴───────┘
┌───────────┬───────┬───────┬─────────┬─────────┬─────────┬─────────┬─────────┐
│ Stat      │ 1%    │ 2.5%  │ 50%     │ 97.5%   │ Avg     │ Stdev   │ Min     │
├───────────┼───────┼───────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Req/Sec   │ 372   │ 372   │ 447     │ 454     │ 439.8   │ 17.39   │ 372     │
├───────────┼───────┼───────┼─────────┼─────────┼─────────┼─────────┼─────────┤
│ Bytes/Sec │ 54 kB │ 54 kB │ 64.8 kB │ 65.9 kB │ 63.8 kB │ 2.52 kB │ 53.9 kB │
└───────────┴───────┴───────┴─────────┴─────────┴─────────┴─────────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 13194 │
└──────┴───────┘

Req/Bytes counts sampled once per second.

13k requests in 30.02s, 1.91 MB read

> gateway@1.0.0 loadtest:grpc:case:12
> npx autocannon -c 10 -d 30 localhost:3000/grpc/write/high-payload --renderStatusCodes

Running 30s test @ http://localhost:3000/grpc/write/high-payload
10 connections

┌─────────┬───────┬───────┬───────┬───────┬──────────┬─────────┬────────┐
│ Stat    │ 2.5%  │ 50%   │ 97.5% │ 99%   │ Avg      │ Stdev   │ Max    │
├─────────┼───────┼───────┼───────┼───────┼──────────┼─────────┼────────┤
│ Latency │ 41 ms │ 51 ms │ 63 ms │ 65 ms │ 51.49 ms │ 6.02 ms │ 127 ms │
└─────────┴───────┴───────┴───────┴───────┴──────────┴─────────┴────────┘
┌───────────┬─────────┬─────────┬───────┬─────────┬─────────┬───────┬─────────┐
│ Stat      │ 1%      │ 2.5%    │ 50%   │ 97.5%   │ Avg     │ Stdev │ Min     │
├───────────┼─────────┼─────────┼───────┼─────────┼─────────┼───────┼─────────┤
│ Req/Sec   │ 176     │ 176     │ 193   │ 201     │ 192.17  │ 5.41  │ 176     │
├───────────┼─────────┼─────────┼───────┼─────────┼─────────┼───────┼─────────┤
│ Bytes/Sec │ 25.5 kB │ 25.5 kB │ 28 kB │ 29.2 kB │ 27.9 kB │ 784 B │ 25.5 kB │
└───────────┴─────────┴─────────┴───────┴─────────┴─────────┴───────┴─────────┘
┌──────┬───────┐
│ Code │ Count │
├──────┼───────┤
│ 200  │ 5765  │
└──────┴───────┘

Req/Bytes counts sampled once per second.

6k requests in 30.02s, 836 kB read