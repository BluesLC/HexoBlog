---
title: FFmpeg学习笔记(一)(草稿)
url: 249.html
id: 249
categories:
  - 未分类
tags:
---

### FFmpeg中较为重要的两个库:

1.  avformat.lib
2.  avcodec.lib

### FFmpeg中较为重要的结构体:

*   AVFormatContext:封装器上下文
*   AVCodecContext:解码器上下文
*   AVIOContext:
*   AVPacket:它保存了解复用之后，解码之前的数据（用于存储压缩的数据）和关于这些数据的一些附加信息，如显示时间戳（pts）、解码时间戳（dts）、数据时长，所在媒体流的索引等。 用于存储压缩的数据，分别包括有音频压缩数据，视频压缩数据和字幕压缩数据。
*   AVFrame:用于存储解码后的音频或者视频数据
*   AVStream

![](http://luchong.xyz/wp-content/uploads/2018/07/20130914204051125-300x122.jpg)

### 函数:

*   avformat\_open\_input()
*   avformat\_close\_input()
*   avformat\_find\_stream_info()
*   av\_find\_best_stream()
*   av\_read\_frame()
*   av\_seek\_frame()

​