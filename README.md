<div align="center">

## Splash Screen


</div>

### Description

Displays a splashscreen for the amount of time you specify, then closes. PLEASE RATE IT.
 
### More Info
 
-int width, is splashscreen width

-int height, is splashscreen heigth

-String imagePath is image location

-int Seconds, is the number of seconds you want

the splash screen to be displayed


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Adisson Ruiz](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/adisson-ruiz.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |Java \(JDK 1\.1\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/adisson-ruiz-splash-screen__2-1871/archive/master.zip)





### Source Code

```
import java.awt.*;
import javax.swing.*;
public class SplashScreen extends JWindow
{
 private SplashScreenImage image;
 private int top, left;
 private int Seconds =1;
 public SplashScreen(int width, int height, String imagePath, int Seconds)
 {
 super.setSize(width, height);
 this.Seconds = Seconds;
 image = new SplashScreenImage(Toolkit.getDefaultToolkit().getImage(imagePath));
 super.getContentPane().add(image);
 top = (super.getToolkit().getScreenSize().height / 2) - (size().height / 2);
 left = (super.getToolkit().getScreenSize().width / 2) - (size().width / 2);
 super.setLocation(top, left);
 image.setSize(width, height);
 }
 public void show()
 {
 super.show();
 try{Thread.sleep(Seconds * 1000);}
 catch(InterruptedException e){}
 super.hide();
 }
}
class SplashScreenImage extends Canvas
{
 Image Splashimage;
 public SplashScreenImage(Image Splashimage)
 {
 this.Splashimage = Splashimage;
 }
 public void paint(Graphics g)
 {
 g.drawImage(Splashimage,0,0,this);
 }
}
```

