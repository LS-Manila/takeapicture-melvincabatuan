# Taking a Picture

takeapicture-melvincabatuan created by Classroom for GitHub

This assignment illustrates the basic usage of built-in camera in Android.


## Problem:

Implement an Android activity for taking a picture and show it in an ImageView.   


## Accept

To accept the assignment, click the following URL:

https://classroom.github.com/assignment-invitations/884489a9965a78e0759d03fca67ddf63

## Sample Solution:

https://github.com/DeLaSalleUniversity-Manila/takeapicture-melvincabatuan

## Keypoints:

Setting up a button onClickListener in Java:
```Java
        Button b = (Button) findViewById(R.id.picbutton);

        b.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent picIntent = new Intent(MediaStore.ACTION_IMAGE_CAPTURE);
                startActivityForResult(picIntent, REQUEST_IMAGE_CAPTURE);
            }
        });
```

Showing the taken image in an ImageView:
```Java
   @Override
    protected void onActivityResult(int requestCode, int resultCode,
                                    Intent intent) {
        if (requestCode == REQUEST_IMAGE_CAPTURE
                && resultCode == RESULT_OK) {
            setContentView(R.layout.activity_pic);
            Bitmap bmp = (Bitmap) intent.getExtras().get("data");
            ImageView img = (ImageView) findViewById(R.id.pictureview);
            img.setImageBitmap(bmp);
        }
    }
```



## Submission Procedure with Git: 

```shell
$ cd /path/to/your/android/app/
$ git init
$ git add –all
$ git commit -m "your message, e.x. Assignment 1 submission"
$ git remote add origin <Assignment link copied from assignment github, e.x. https://github.com/DeLaSalleUniversity-Manila/secondactivityassignment-melvincabatuan.git>
$ git push -u origin master
<then Enter Username and Password>
```


## Screenshot:

![alt tag](https://github.com/DeLaSalleUniversity-Manila/takeapicture-melvincabatuan/blob/master/device-2015-10-08-232651.png)

![alt tag](https://github.com/DeLaSalleUniversity-Manila/takeapicture-melvincabatuan/blob/master/device-2015-10-08-232746.png)

![alt tag](https://github.com/DeLaSalleUniversity-Manila/takeapicture-melvincabatuan/blob/master/device-2015-10-08-232833.png)

"*I would rather die of passion than of boredom.*" - Vincent van Gogh
