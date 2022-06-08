# projet
client léger
<?php
    include("navbar.php");
    include("database.php");
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="../css/style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="icon" type="image/png" sizes="16x16 32x32" href="img/logo.png">
    <title>Acceuil - FAST PERMIS</title>
</head>
<body>
    <header>
        
        <nav>
            <a href="acceuil"><img src="../img/logo.png"  class="logo" alt=""></a>
            <ul class="nav__links">            
                <li class="nav-item ">
                    <a class="nav-link one" href="code.php">Code</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="permis.php">Permis</a>
                </li>
                
                <li class="nav-item">
                    <a class="nav-link" href="contact.php">Contact</a>
                </li>
                <?php
                    echo $btn_menu;
                ?>
                
            </ul>
            
        </nav>
    </header>
    <div class="presentation">
        <div class="back">
            <div class="filtre"></div>
            <h1 class="hero">L'auto-école en nettement mieux</h1>
            <h2 class="hero2">Obtenez votre permis en moins de <span class="warning">3 semaines</span> !</h2>
            <div class="back-img">
                <img src="img/1.jpg" alt="">
            </div>
        </div>
        <div class="offre">
        <div class="row">
            <div class="card">
                <h3 class="card-title">Code de la route</h3>
                <p class="card-text">à partir de <span class="prix">
                    <?php
                        $req= "select prix_f from formule where nom_f = 'code de la route'";
                        $result = mysqli_query($con,$req);
                        while($ligne = mysqli_fetch_array($result)){            
                            echo $ligne['prix_f']."€";
                        }
                    ?>
                </span></p>
                <a href="permis.php" class="btn ">Découvrir nos offres</a>
                <a href="#" class="card-link">Nos tarifs Code</a>
            </div>
            <div class="card">
                <h3 class="card-title">Permis de conduire</h3>
                <p class="card-text">à partir de <span class="prix">
                    <?php
                        $req= "select prix_f from formule where nom_f = 'permis de conduire'";
                        $result = mysqli_query($con,$req);
                        while($ligne = mysqli_fetch_array($result)){            
                            echo $ligne['prix_f']."€";
                        }
                    ?>
                </span></p>
                <a href="permis.php" class="btn btn-warning">Découvrir nos offres</a>
                <a href="#" class="card-link">Nos tarifs Permis</a>
            </div>
        </div>
    </div>
        <div class="desc">
            <h1 class="title-desc">Une formation flexible et personnalisée</h1><br>
            <div class="row1">
                <div class="part">
                    
                    <div class="cercle">
                        <img src="../img/responsive.png" class="reviser" alt="Révisez où et quand vous voulez">
                    </div>
                    <h3>Révisez le code où et quand vous voulez</h3>
                    <span>Entraînez-vous au Code de la route <br>intégralement en ligne ou dans nos <br>agences.</span>
                </div>

                <div class="part">
                    
                    <div class="cercle">
                        <img src="../img/learn.webp" class="learn" alt="Auto-école partout en France" title="Auto-école partout en France">
                    </div>
                    <h3>Apprenez à conduire ici, là, ou même ailleurs</h3>
                    <span>Nos moniteurs d'auto école passent <br>vous prendre dans l’un des 565 <br>points de rendez-vous, partout en <br>France.</span>
                </div>

                <div class="part">
                    
                    <div class="cercle">
                        <img src="../img/solution.webp" class="solution" alt="Payez votre permis de conduire en plusieurs fois" title="Payez votre permis de conduire en plusieurs fois">
                    </div>
                    <h3>Bénéficiez de solutions flexibles et économiques</h3>
                    <span>Des packs permis de conduire tout compris dès 549€ et la possibilité de payer en deux ou trois fois sans frais.</span>
                </div>
            </div>
        </div>
    </div>
    

    <div class="red">
        <h1>Bénéficiez de solutions flexibles et économiques</h1>
        <div class="row2">
            <div class="part2">
                <img src="../img/satisfaction.webp" alt="">
                <h3>14 jours pour changer d’avis</h3>
                <p class="descriptif">Si vous prenez un pack permis, vous avez 14 jours après votre premier cours (évaluation initiale) pour changer d’avis et être remboursé à 100%</p>
            </div>

            <div class="part2">
                <img src="../img/euros.webp" alt="">
                <h3>Paiement en plusieurs fois</h3>
                <p class="descriptif">Paiement en 3 fois par carte bancaire ou en 6 fois par chèque disponible pour tout paiement supérieur à 330 € d’achat.</p>
            </div>

            <div class="part2">
                <img src="../img/valid.webp" alt="">
                <h3>Garantie financière</h3>
                <p>Depuis toujours, nous assurons le remboursement en cas d’imprévus.</p>
            </div>
            <div class="part2">
                <img src="../img/lock.webp" alt="">
                <h3>Paiement sécurisé</h3>
                <p class="descriptif">Effectuez vos paiements en ligne en toute sécurité</p>
            </div>
        </div>
    </div>

    <footer>
            <ul class="link-one">
                <li><a href="">Code de la route</a></li>
                <li><a href="">Permis</a></li>
                <li><a href="">Tarifs</a></li>
                <li><a href="">Contact</a></li>
                <li><a href="">Nos localisations</a></li>
            </ul>
        
            <a href ="contact.php"><div class="btn-r">Recrutement</div></a>
            <ul class="link-two">
                <li><a href="">Plan du site</a></li>
                <li><a href="">Mentions légales</a></li>
                <li><a href="">CGV</a></li>
                <li><a href="contact.php">Contact</a></li>
            </ul>   
    </footer>
    <script src="../js/script.js"></script>
</body>

</html>
