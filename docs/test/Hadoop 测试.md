# Hadoop 测试

## MR

- tergen

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar teragen 100 /tmp/out123
```
参数1 表示生成的行数，每行100B

参数2 输出目录

- terasort

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar terasort -Dmapred.reduce.tasks=100 input output
```

- teravalidate(对排序的结果进行验证)

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar teravalidate input output
```

- wordCount

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar wordcount /test/in /tmp/o1
```

- pi

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar pi -Dmapreduce.job.queuename=root.test_queue1 1 1000
```

- sliveTest

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-client-jobclient-2.7.1-tests.jar SliveTest  -maps 2 -ops 2 -files 1000000000 -baseDir /tmp/007  -delete 0 -mkdir 100 -create 0  -append 0 -rename 0 -read 0 -ls 0 -truncate 0
```

- TestDFSIO

```bash
hadoop jar /software/servers/hadoop-2.7.1/share/hadoop/mapreduce/hadoop-mapreduce-client-jobclient-2.7.1-tests.jar TestDFSIO
```

