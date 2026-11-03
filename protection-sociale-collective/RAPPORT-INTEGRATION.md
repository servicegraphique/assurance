# Intégration de protection-sociale-collective

Landing page dupliquée depuis `assurance-tns` et adaptée pour la **Protection sociale collective** (Mutuelle collective, Prévoyance collective, Retraite supplémentaire).

Le formulaire multi-étapes et le design sont conservés et enrichis avec les sections dédiées employeur. `lead-handler.js` et `verification-sms.js` assurent la capture et la vérification SMS. Le conteneur GTM `GTM-53SH7D7F` est chargé après le Consent Mode V2 par défaut.

- Identité CRM : `ADW_LP_PROTECTION_SOCIALE_COLLECTIVE` (à valider/enregistrer côté CRM).
- Source de secours : `LP Protection Sociale Collective`.
- Filtre GTM micro-entrepreneur conservé via `microField: 'reponse_3'`.
- Questions retirées conformément au brief : *Quel est votre régime actuel ?* (`question_2`) et *Seriez-vous également intéressé par les assurances professionnelles ? Lesquelles ?* (`question_5`).
- CRM : URL et mode dans `lead-handler.js` (`UBE_CONFIG`, surcharge possible par `window.UBE_CONFIG_OVERRIDE`). Le mode par défaut `nocors` ne confirme pas la réception.
- Google Sheets : URL Apps Script dans `lead-handler.js` ; confirmer la feuille et ses droits.
- SMS : URL et délai dans `verification-sms.js` ; confirmer CORS et tester un vrai SMS sur le domaine final.
