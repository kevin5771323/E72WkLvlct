## 前言

欢迎来到“黄师日报”平安小程序项目，此项目基于Spring Boot框架开发，结合了微信小程序、Vue、Uniapp等前端技术，旨在为广大用户提供便捷、高效的日报查询服务。以下是本项目的详细说明。

## 内容介绍

“黄师日报”平安小程序是一款基于Java语言的日报查询应用，用户可以通过微信小程序端查看每日安全日报信息。系统后端采用Spring、Springmvc、MyBatis等主流框架，确保了系统的高效、稳定运行。前端则使用JS、Vue、CSS3、Uniapp等技术，实现了良好的用户体验。

## 技术介绍

- 语言：Java
- 使用框架：Spring、Springmvc、MyBatis，微信小程序
- 前端技术：JS、Vue、CSS3，Uniapp
- 开发工具：IDEA/Eclipse，Uniapp
- 数据库：MySQL 5.7/8.0
- 数据库管理工具：phpstudy/Navicat
- JDK版本：jdk1.8
- Maven：apache-maven 3.8.1-bin
- 前端环境：Node.Js 12\14\16

## 核心代码

以下是项目中的一个核心代码片段，展示了如何通过MyBatis实现日报信息的查询：

```java
// Mapper接口
public interface DailyReportMapper {
    @Select("SELECT * FROM daily_report WHERE date = #{date}")
    DailyReport getDailyReportByDate(@Param("date") String date);
}

// Service层
@Service
public class DailyReportService {
    @Autowired
    private DailyReportMapper dailyReportMapper;

    public DailyReport getDailyReportByDate(String date) {
        return dailyReportMapper.getDailyReportByDate(date);
    }
}

// Controller层
@RestController
@RequestMapping("/dailyReport")
public class DailyReportController {
    @Autowired
    private DailyReportService dailyReportService;

    @GetMapping("/{date}")
    public ResponseEntity<DailyReport> getDailyReportByDate(@PathVariable String date) {
        DailyReport dailyReport = dailyReportService.getDailyReportByDate(date);
        return ResponseEntity.ok(dailyReport);
    }
}
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

## 项目截图
![封面图片](https://img13.360buyimg.com/ddimg/jfs/t1/335046/11/13013/207198/68c57fd2Fcc9acf2d/52c305f22b9ce79b.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/343249/4/3164/59116/68c57faaF526e779e/8052d99ecf170ea9.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/333236/27/12953/48891/68c57faaF23b5aeb2/aaccea12fea5f6c3.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/339274/4/10399/66100/68c57faaFd51b1727/539ad27907fa0516.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/337225/39/10469/93597/68c57fabF8d461bcb/c0697b45190be88e.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/349683/2/3031/15352/68c57fabF7dedf978/c5a93b17208488be.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/323510/5/19842/9357/68c57fabF1a73a940/348d2741a8f72ecf.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/345958/12/3037/15862/68c57fabFbc5808eb/2643e79942c760f3.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/330823/2/12822/47368/68c57fabF9b9fe411/516b85108ab37626.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/337391/27/9866/66530/68c57facFd6f878da/f93511e2e6803507.jpg)


## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
