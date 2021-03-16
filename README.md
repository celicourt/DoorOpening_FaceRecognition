# DoorOpening_FaceRecognition

# Introduction Générale
                            
Le système de sécurité domestique est devenu essentiel pour chaque maison. Jusqu'à présent, la plupart des portes pouvaient être ouvertes par des moyens conventionnels, tels que des clés, des cartes de sécurité, des mots de passe ou des échantillons. Cependant, des incidents tels que la perte d'une clé ont créé de graves problèmes, tels que le vol d'identité et la fraude. C'est devenu un gros problème. Pour résoudre ce problème, la reconnaissance faciale a été introduite à l'aide de la technologie d'apprentissage en profondeur et l'Internet des objets (IoT) a également été utilisé pour faire fonctionner un système de contrôle d'accès de porte efficace. Raspberry Pi est une petite carte d'ordinateur programmable qui est utilisée comme contrôleur principal pour la reconnaissance faciale, le système de verrouillage. L'appareil photo prend des photos de la personne devant la porte. Le système IoT permet à l'utilisateur de contrôler l'accès à la porte. La reconnaissance faciale est l'un des systèmes d'identification biométrique les plus utilisés avec les empreintes digitales. 

# Analyse du problème
Dans le monde des technologies émergentes, la sécurité est devenue une composante de la vie quotidienne. Vol de l'information, manque de sécurité et violation de la vie privée, etc. Ce sont les éléments essentiels qui devraient être protégés. L'utilisation de systèmes sûrs intelligents pour bloquer et déverrouiller les portes est populaire aujourd'hui. Ce système est adapté par plusieurs pays et première classe, tels que, le Japon, les États-Unis, etc. qui utilisent déjà le système. Ce système fournit une fonction de sécurité pour la reconnaissance faciale, soit un clavier est fourni pour entrer le  code d'accès pour déverrouiller la porte.

# Solution proposée 
Spécification du problème
Aujourd’hui, l'utilisation de cartes magnétiques, de clés ou de badges  n'échappe pas au risque de vol par des fraudeurs qui peuvent tromper leur identité de manière remarquable. 
Toutefois, ces difficultés ont conduit à l'idée d'utiliser les ressources biométriques comme moyen d'identification. En fait, chaque individu a des caractéristiques uniques: la voix, les empreintes digitales, les traits du visage, la forme de la main par rapport à l'ADN, etc. Ces données sont appelées biométriques et peuvent donc être utilisées pour l'identification. 
Au cours de ces dernières décennies, une personne doit être identifiée dans divers contextes pour entrer dans un immeuble ou ouvrir la porte de sa maison et se déplacer librement là où la sécurité est nécessaire. 
Cependant, le visage est certainement la caractéristique biométrique que les gens utilisent le plus naturellement pour s'identifier. La reconnaissance faciale est donc devenue l'un des domaines de vision par ordinateur les plus performants et les plus dynamiques.

# Solution proposé de notre système
Pour notre système, nous concevons un système de déverrouillage des portes à l'aide du module de reconnaissance faciale. Dans notre cas, nous avons utilisé Raspberry pi avec de nombreuses fonctionnalités qui permettent à l'utilisateur de modifier l'utilisation dans divers programmes intelligents. 

# Méthodologie
## Algorithme utilisé
Pour réaliser notre travail, nous avons utilisé en premier lieu l'algorithme HOG (Histogram of Oriented Gradients ) pour faire la détection du visage dans une image. Nous avons commencé par rendre notre image en noir et blanc, ensuite nous avons examiné chaque pixel de notre image un par un pour pouvoir regarder tous les pixels qui entourent chaque pixel. Ainsi, on peut déterminer à quel point le pixel actuel est sombre par rapport aux pixels qui l'entourent directement. Ensuite, dessinons une flèche indiquant dans quelle direction l'image s'assombrit, ainsi on détermine le gradient.

# Technique
Dans notre cas, nous prenons au moins une seule image pour chaque utilisateur, ou plusieurs dans différents contextes, elles sont toutes stockées dans notre base de données qui comporte une classe pour chaque utilisateur. 
Puis, on fait l’entrainement des images dont nous disposons dans notre base d’images selon la méthodologie décrite dans le point précédente. Les données dérivées de l’entrainement sont sauvegardées sous forme de fichier
La même méthodologie utilisée pour faire l’entrainement est utilisée lors de l’exécution de l’application pour pouvoir faire la comparaison entre les données de l’image qu’il y a entrée et les données d’entrainement.
S’il y a correspondance, un encadré apparaît autour de la face de l’utilisateur étiqueté par son nom suivi de Door Open.
