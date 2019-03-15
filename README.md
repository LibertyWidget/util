
<pre>
    <code>
        this.mRotateAnimation = new RotateAnimation(
                0f, /*起始角度 0*/
                -360f, /*旋转角度 -60度*/
                Animation.RELATIVE_TO_SELF,/*相对于自身 Animation.RELATIVE_TO_PARENT(相对于父控件*/
                0.5f,   /* 中心点  缩放动画围绕X方向的中心点，当为数值时，表明是屏幕上的绝对坐标值，当为百分数（如50%）时，为相对自己本身控件的比例值，当为百分数加p（如50%p）时，为相对父布局的比例值*/
//                Animation.RELATIVE_TO_PARENT,/*相对于父控件*/
                Animation.RELATIVE_TO_SELF,/*相对于自身*/
                0.5f);/*中心点*/
        this.mRotateAnimation.setDuration(1000);/*持续时间*/
//        this.mRotateAnimation.setRepeatCount(1);/*重复一次*/
//        this.mRotateAnimation.setRepeatMode(Animation.RESTART);/*重复*/
        this.mRotateAnimation.setFillAfter(true);/*停留在最后*/
        this.mRotateAnimation.setStartOffset(0);/*延迟执行*/
//        this.mRotateAnimation.setDetachWallpaper(true);/*未知*/
        /*正在播放的动画内容保持当前的Z轴顺序， normal top bottom*/
        this.mRotateAnimation.setZAdjustment(Animation.ZORDER_NORMAL);/*允许在动画播放期间，调整播放内容在Z轴方向的顺序*/
    </code>
<pre>

        <set xmlns:android="http://schemas.android.com/apk/res/android"
            android:duration="1000"
            android:fillAfter="true"
            android:repeatMode="restart"
            android:startOffset="1000">

            <!-- duration    执行时间     单位毫秒 -->
            <!-- fillAfter   是否停留在最后一帧 true -->
            <!-- startOffset 是否延迟执行 单位毫秒 -->
            <!-- repeatMode  reverse(倒序)和restart(重复) 必须配合repeatCount一起使用-->
            <alpha
                android:fromAlpha="1"
                android:toAlpha="0" />
            <!-- fromAlpha 开始透明度-->
            <!-- toAlpha 结束透明度-->
            <rotate
                android:fromDegrees="90"
                android:pivotX="50%"
                android:pivotY="50%"
                android:toDegrees="0" />

            <!-- fromDegrees 正数为顺时针，负数为逆时针  360-->
            <!-- toDegrees 动画结束时的角度  360-->
            <!-- pivotX 中心点  缩放动画围绕X方向的中心点，当为数值时，表明是屏幕上的绝对坐标值，当为百分数（如50%）时，
            为相对自己本身控件的比例值，当为百分数加p（如50%p）时，为相对父布局的比例值-->
            <!-- pivotY 中心点-->

            <scale
                android:fromXScale="0"
                android:fromYScale="0"
                android:pivotX="50%"
                android:pivotY="50%"
                android:toXScale="1.5"
                android:toYScale="1.5" />

            <!-- fromXScale 动画开始前的X方向上的尺寸-->
            <!-- fromYScale 动画开始前的Y方向上的尺寸-->

            <!-- pivotX 中心点  缩放动画围绕X方向的中心点，当为数值时，表明是屏幕上的绝对坐标值，当为百分数（如50%）时，
               为相对自己本身控件的比例值，当为百分数加p（如50%p）时，为相对父布局的比例值-->

            <translate
                android:fromXDelta="0"
                android:fromYDelta="0"
                android:toXDelta="1.5"
                android:toYDelta="1.5" />

        </set>