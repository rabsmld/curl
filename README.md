
curl_setopt($ch, CURLOPT_POSTFIELDS, $postfields);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true); //to suppress the curl output
$result = curl_exec($ch);
curl_close ($ch);
