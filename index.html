<?php
error_reporting(0);	    //MENGHANDLE PESAN ERROR LINE 43-48 KARNA UNDEFINED(IS PHP NOT JS)
session_start();        //MEMULAI SESSION
include './pages/koneksi/config.php';  //MENYERTAKAN FILE KONEKSI

//SESSION LOGIN/LOGOUT
if (isset($_COOKIE['id']) && isset($_COOKIE['key'])) {  //JIKA ID DAN KEY BERNILAI TRUE LAKUKAN
    $id = $_COOKIE['id'];                               //MENYIMPAN VALUE ID
    $key = $_COOKIE['key'];                             //MENYIMPAN VALUE KEY

    $query = mysqli_query($db, "SELECT * FROM tb_admin WHERE id= $id");   //QUERY MENCARI DATA BERDASARKAN ID
    $data = mysqli_fetch_assoc($query);                 //MENGAMBIL LIST DATA DARI QUERY
    $season_id = hash('sha1', $data['password']);       //ENKRIPSI SHA1 MENJADI CHIPERTEXT DARI QUERY PASSWORD
    
    if ($key == $season_id) {                           //JIKA KEY DAN SEASON ID TRUE LAKUKAN
        $_SESSION['level'] = $data['level'];            //MENYIMPAN SESSION LEVEL 
    }
}

//LOGIN
if (isset($_POST['login'])) {
    //mencegah user jahat untuk menyisipkan tag html/js dari serangan XSS bisa juga htmlspecialchars(komentar)
    $user_xss = strip_tags($_POST['username']);
  
    //mysql_real_escape_string = mencegah sql injection '=' / '=''or' / 'or''='
    $username = mysqli_real_escape_string($db, $user_xss);
    
    //md5 enkripsi untuk mengamankan password dari admin agar privasi terjaga
    $password = mysqli_real_escape_string($db, md5($_POST['password']));
    
    $query = mysqli_query($db,"SELECT * FROM tb_admin WHERE username='$username' AND password='$password'");
    $data = mysqli_fetch_assoc($query);

    if ($username === $data['username']) {
        if ($password === $data['password']) {
            if (isset($_POST['remember'])) {            //JIKA CEKLIS REMEMBER ME LAKUKAN
                //BUAT COOKIE 60detik * 60menit = sejam dalam hitungan detik(3600)
                //BUAT COOKIE 3600detik * 24 = sehari dalam hitungan detik(86400) * 1hari
                setcookie('id', $data['id'], time() + 60 * 60 * 24 * 1);
                setcookie('key', hash('sha1', $data['password']), time() + 60 * 60 * 24 * 1);
            }
            $_SESSION['level'] = $data['level'];        //LOGIN TANPA CEKLIS REMEMBER ME(SESSION)
        }
    } else {
        header('Location:index.php');
    }
}
if (isset($_SESSION['level'])) {                        //LOGIN TANPA CEKLIS REMEMBER ME
    header('Location: ./pages/main/dashboard.php');                  //MASUK KE DASHBOARD LEWAT SEASON LOGIN
}

//LOGOUT
if (isset($_GET['logout'])) {
    session_unset();
    session_destroy();
    setcookie('id','', time() + 60 * 60 * 24 * 1);
    setcookie('key','', time() + 60 * 60 * 24 * 1);
    header('Location: index.php');
}
?>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="style/bootstrap.min.css">
    <link rel="stylesheet" href="style/custom.css">
</head>

<body>
    <div class="login-container col-lg-4 col-md-6 col-sm-8 col-xs-12">
        <div class="login-title text-center">
        </div>
        <div class="login-content">
            <div class="login-header ">
                <h3><strong>Welcome,</strong></h3>
                <h5>Silahkan Masuk Ke Dashboard</h5>
            </div>
            <div class="login-body">

                <form action="" method="POST">
                    <div class="form-group ">
                        <div class="pos-r">
                            <input id="form-username" type="text" name="username" placeholder="Username..."
                                class="form-username form-control">
                        </div>
                    </div>
                    <div class="form-group">
                        <div class="pos-r">
                            <input id="form-password" type="password" name="password" placeholder="Password..."
                                class="form-password form-control">
                        </div>
                    </div>

                    <div class="form-group">
                        <button type="submit" class="btn btn-primary form-control" name="login"><strong>Sign
                                in</strong></button>
                    </div>
                    <div class="login-footer text-center template">
                        <!--<h5><a href="index.php" class="bold"> Kembali Ke Home </a></h5>   -->
                    </div>
                </form>

            </div> <!-- end  login-body -->
        </div><!-- end  login-content -->
        <div class="login-footer text-center template">
            <div class="login-footer text-center template">
            </div>
        </div> <!-- end  login-container -->
    </div>
    </div><!-- end container -->
</body>

</html>
