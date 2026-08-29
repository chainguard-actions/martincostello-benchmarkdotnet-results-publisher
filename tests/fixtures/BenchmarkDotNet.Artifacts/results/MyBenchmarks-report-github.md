```

BenchmarkDotNet v0.14.0, Ubuntu 22.04
Intel Core i7, 1 CPU, 8 logical and 4 physical cores
.NET SDK 8.0.401
  [Host]     : .NET 8.0.8 (8.0.824.36612), X64 RyuJIT AVX2
  DefaultJob : .NET 8.0.8 (8.0.824.36612), X64 RyuJIT AVX2

```
| Method       | input | Mean     | Error    | StdDev   | Gen0 | Allocated |
|------------- |------ |---------:|---------:|---------:|-----:|----------:|
| **RunBenchmark** | **001**   | **100.5 ns** | **12.96 ns** | **0.710 ns** |    **-** |      **24 B** |
