http://www.brendangregg.com/FlameGraphs/cpuflamegraphs.html
通过profiler工具　提供优化的存在问题
profiler:
perf
dtrace
systemtap
Vtune

vtune amplifier
Oprofile
gprof
tcpdump
strace
dstat iostat top sar

如何使用Valgrind memcheck工具进行C/C++的内存泄漏检测
kcachegrind
将结果展现在页面上
提供PID　定位其性能问题所在，
Java详细至线程堆栈

sudo perf record -F 99 -a -g -- sleep 60
sudo perf script -f > out.perf
./flamegraph.pl out.perf > kernel.svg
./stackcollapse-perf.pl out.perf > out.folded
./flamegraph.pl out.folded > kernel.svg

Java 
JVM profilers: like hprof, LJP, and commercial profilers. These show Java methods, but usually not system code paths
