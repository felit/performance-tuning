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


将结果展现在页面上
提供PID　定位其性能问题所在，
Java详细至线程堆栈

sudo perf record -F 99 -a -g -- sleep 60
sudo perf script -f > out.perf
./flamegraph.pl out.perf > kernel.svg
./stackcollapse-perf.pl out.perf > out.folded
./flamegraph.pl out.folded > kernel.svg
