if (isset($_GET[‘code’]))

{
$c = curl_init();

$postfields = array(
‘client_id’ => ‘0ffdc29d06e24a2ea9beab9e65236da1
’,
‘client_secret’ => ‘f50ede4706cb43cdbf608fed704d41d7’,
‘grant_type’ => ‘authorization_code’,
‘code’ => $_GET[‘code’],
‘redirect_uri’ => ‘https://www.instagram.com/rabsmld/’
);

$url = « https://api.instagram.com/oauth/access_token »;

$ch = curl_init();

// EXECUTE THE CURL…
curl_setopt($ch, CURLOPT_URL,$url);
curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, FALSE);
curl_setopt($ch, CURLOPT_SSL_VERIFYHOST, 2);
curl_setopt($ch, CURLOPT_POST, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, $postfields);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true); //to suppress the curl output
$result = curl_exec($ch);
curl_close ($ch);
