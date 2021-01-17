# <p align="center"> كتابة خوارزمية ربط الواجهة مع معالج التحكم بالمحركات </p>

### <div dir="rtl">  هذه الخوارزمية لطريقة مبدئية لطريقة ربط الواجهة التي نفذتها بلغات برمجة الويب أو سطح المكتب</div>
### <div dir="rtl"> تمت هذه المهمة لجزء من مشروع أثناء التدريب الثاني في شركة الأساليب الذكية في مسار إنترنت الأشياء 💡</div>

#### <div dir="rtl"> </div>

#### <p  dir="rtl"> [ واجهة الويب المرتبطة بقواعد البيانات باستخدام PHP و HTML و CSS  مع قواعد بيانات MySQL ](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/tree/main/Control%20panel%20for%20robot%20arm%20with%20database)</p>


#### <p dir="rtl"> [ واجهة سطح المكتب المرتبطة بقواعد البيانات باستخدام C#  مع قواعد بيانات MySQL ](https://github.com/MohammadYAmmar/A-control-panel-program-for-robot-arm-with-databases-for-Windows-devices-via-c-sharp)</p>



### <div dir="rtl">يتطلب علبنا لتصور العمل إن ننفذ مخطط تدفقي (Flowchart) لتحليل ما سيتحدث بشكل مبسط </div>


![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Algorithm:%20Connecting%20interface%20to%20IoT/%D8%B5%D9%88%D8%B1%D8%A9%20%D9%84%D9%84%D9%85%D8%AE%D8%B7%D8%B7%20%D8%A7%D9%84%D8%AA%D8%AF%D9%81%D9%82%D9%8A.png) 


### <div dir="rtl">* من الممكن إستخدام أمر Ping للتأكد عن إن الجهاز متواجد ما قبل ذلك أيضًا </div>



## <div dir="rtl">والمتطلبات هي كما في الرسم التوضيحي (Diagram) سوف تكون عبارة عن الجهاز للمستخدم مثل أجهزة الحاسب الآلي أو عبر تطبيق بالهواتف الذكية متصلة بقاعدة البيانات والتي سوف يقرأ منها أجهزة ذراع التحكم لتنفيذ ما يرسل لها</div>

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Algorithm:%20Connecting%20interface%20to%20IoT/Image%20of%20project%20diagram.png) 

## <div dir="rtl">عند الرغبة في تنفيذ ذلك برمجياً علينا تعديل العمليات التي سوف تحدث عن النقر على الزر المسؤول عن ذلك </div>

## <div dir="rtl">في الموقع الإلكتروني </div>

`if (isset($_POST['run-submit'])) {
	//Send commands to databases
	echo("");			
		}`


## <div dir="rtl">في برنامج سطح المكتب </div>
`private void run_button_Click(object sender, EventArgs e)
        {
            /*
             * Here the bot communication for transmission and motor movement will be included through HTTP commands
             */
        }`


## <div dir="rtl">مصادر: </div>

## <div dir="rtl">1 - قالب الرسم التوضيحي </div>

network/citrix.xml in program draw.io Diagrams

## <div dir="rtl">2 - موقع تم استخدامه للصور</div>

https://icons8.com/
