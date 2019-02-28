# phpqrcode
二维码生成类
初始化
`$code = new PHPQRCode\QRcode(); `
`$code->png('二维码内容，链接文本等等','二维码存放路径');  `

```
$qr_code_path = UPLOAD_PATH.'qr_code/';
        if(!file_exists($qr_code_path)){
            mkdir($qr_code_path);
        }
        $qr_code_file = $qr_code_path.time().rand(1,10000).'.png';
        $code = new QRcode();
        $code->png($data,$qr_code_file);
        echo '<img alt="模式二扫码支付" src="'.SITE_URL.'/'.$qr_code_file.'" style="width:110px;height:110px;"/>';
        //$qrHandle = imagecreatefromstring(file_get_contents($qr_code_file));
        unlink($qr_code_file); //删除二维码文件
//        header("Content-type: image/png");
//        imagepng($qrHandle);
//        imagedestroy($qrHandle);

```
