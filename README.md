# Implied-and-surface-volatility-in-BS-and-Heston-models

Le but de ce projet était d'apprendre par GPR (gaussian processing regression) la volatilité implicite et la surface de volatilité dans les modèles de Black & Scholes et Heston. On s'est rendu compte que la volatilité dans le modèle de BS est constante et dans le modèle de Heston elle est variable et la l'allure d'un smile.


## Volatilité et surface de volatilité dans le modèle de BS

**La volatilité implicite** est la valeur de la volatilité qui, lorsqu'elle est insérée dans l'équation de Black-Scholes ou autre modèle, donne le prix de marché actuel de l'option.
Il faut trouver $\sigma$ tel que  

$$ P - BS\(S, K, T, r, \sigma)  = 0 $$

pour $S, K, T, r$ fixé (pour la **surface de volatilité** $K$ et $T$ varient), où $BS\(S, K, T, r, \sigma)$ est le prix de Black&Scholes

## Volatilité dans le modèle de Heston

Le modèle de Heston introduit une équation stochastique pour la volatilité \( v(t) \), donnée par :

$$\ dv(t) = \kappa(\theta - v(t))dt + \sigma \sqrt{v(t)}dW_2(t) \$$

où :

$kappa$ est le coefficient de vitesse de la volatilité,

$theta$ est la longue volatilité,

$sigma$ est la volatilité de la volatilité,

$W_1(t)$ et $W_2(t)$ sont des mouvements browniens standard sous la probabilité risque-neutre, et \( \rho \) est le coefficient de corrélation entre les deux mouvements browniens.

## Métrique 
La métrique utilisée ici est la **RMSE**  (l'erreur quatratique moyenne)
