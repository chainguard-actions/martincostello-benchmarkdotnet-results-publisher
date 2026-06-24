``` ini

BenchmarkDotNet=v0.13.12, OS=ubuntu 22.04
Intel Core i7, 1 CPU, 8 logical and 4 physical cores
.NET SDK=8.0.0
  [Host]     : .NET 8.0.0 (8.0.0.0), X64 RyuJIT AVX2
  DefaultJob : .NET 8.0.0 (8.0.0.0), X64 RyuJIT AVX2
```

| Method       | Mean    | Error   | StdDev  | Allocated |
|------------- |--------:|--------:|--------:|----------:|
| RunBenchmark | 105.5 ns | 0.98 ns | 5.00 ns | 256 B     |
