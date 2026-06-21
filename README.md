# 🎲 Hardware Entropy Mixing Demo (C)

**Concept :** Expérimentation sur la génération de nombres pseudo-aléatoires matériels.
**Objectif :** Démontrer le brassage de sources d'entropie faibles (ASLR et ticks CPU).

**Note de sécurité :**
Ce code est strictement éducatif. Il simule une tentative de génération de clé en combinant le bruit spatial (adresses mémoire via ASLR) et le bruit temporel (horloge CPU). Ce mécanisme n'est **pas** cryptographiquement sécurisé (les bits de poids fort de l'ASLR sont trop prévisibles et le `clock()` manque de résolution). Dans un environnement de production, ce module doit être remplacé par des appels à `/dev/urandom` (POSIX) ou à l'instruction matérielle `RDRAND`.
