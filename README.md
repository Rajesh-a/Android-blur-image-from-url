# Android-blur-image-from-url
Android blur image from url

### Steps:
1. Get Image Url
2. Getting bitmap from image url
3. Blur that bitmap
4. Set blurred image in image view

### How to use in Activity
```` 
 try{
      Bitmap bitmap = new BitmapFromURL().getBitmapFromURL(imgUrl);   
      Bitmap bitmapBlur = new BlurImage().blur(this, bitmap, 20f); // // radius should be >0.0F && <= 25.0F  
      imageView.setImageBitmap(bitmapBlur);
  }
  catch (Exception e){
      e.printStackTrace();   
  }
```` 

//---Note--- Add Thread policy in class before adding code for converting url to bitmap-----------//
```` 
StrictMode.ThreadPolicy policy = new StrictMode.ThreadPolicy.Builder().permitAll().build();
StrictMode.setThreadPolicy(policy);
```` 
