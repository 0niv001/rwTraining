Comparing performance of system to a baseline. 

Used to identify bottlenecks and optimising code. 

*Challenges*
- Hardware and software variability - Choose representative systems making sure results are generalisable. 
- Lack of standard benchmarking tools - difficult to compare results across different systems. 
- Unrealistic or inaccurate benchmark scenarios - Design benchmark scenarios representative of real world workloads. 

Microbenchmarks allow for benchmarking and testing of small code snippets. 
Unit tests can also be used. 
Profiling tools can be used to analyse and optimise performance - Bottlenecks, memory leaks. 

*Features*
- Benchmark modes: Throughput, average time (most used, can use constants), single shot (no warmup). 
- Parameterisation: Run same benchmark for different input values. 
- Profiling: Identify bottlenecks and optimise accordingly. 

Add as dependency in Gradle or Maven. 

*Structure*
- Method with @Benchmark Annotation. 
- Method should have return value. 
- Code to be benchmarked, needs to be inside the method. 

*Annotations*
- State: Specify state object for benchmark
- Setup: Set up state object before running benchmark scenarios
- TearDown:
- Param:

Can use different configuration parameters to customise Benchmark scenarios in JMH. 
Includes number of iterations, warmup iterations, measurement of time. 

Runner makes it easy to run benchmarks from cmd. 

*Common Mistake*
- Not warming up JVM - can lead to inaccurate results. 
- Not controlling external factors, e.g. network latency. 

*Performance bottle necks*
- Slow methods
- Inefficient algorithms - The fewer logic steps the better. 


*State*
- Initialise vars that benchmark code needs, but do nt want  to be part of code, these are state vars
- State objects can be reused across calls to benchmark methods
- JMH gives different scopes that state object can be reused in. 
- State scope is specified in parameter of @state annotation. 
	- Thread: each thread will create own instance of state object
	- Group: Each thread group running the benchmark will create own instance of state object
	- Benchmark: All threads running share same state object
- Requirements:
	- Class needs to be public
	- If nested has to be static
	- Public no args constructor (no parameters to constructors)
```java
@State(Scope.Thread)
class

```

Always create other DB when testing, do not test on live data. 

*Dead Code Elimination*
- Compilers can optimise redundant code. 

!!Boolean Algebra