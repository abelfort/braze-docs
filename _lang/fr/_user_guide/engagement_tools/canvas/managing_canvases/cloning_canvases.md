---
nav_title: Clonage des Canvas
article_title: Clonage des Canvas
page_order: 0
alias: "/cloning_canvases/"
description: "Cet article de référence décrit comment cloner un Canvas depuis l’éditeur Canvas d’origine vers le flux de travail Canvas Flow."
tool: Canvas

---

# Clonage des Canvas vers Canvas Flow

Si vous disposez d’un Canvas de l’éditeur d’origine, vous pouvez le cloner pour créer une copie dans Canvas Flow. En basculant vers le flux de travail Canvas Flow, vous avez accès à des [composants Canvas]({{site.baseurl}}/user_guide/engagement_tools/canvas/canvas_components) légers, des [propriétés d’entrées persistantes]({{site.baseurl}}/user_guide/engagement_tools/canvas/create_a_canvas/canvas_persistent_entry_properties/) et [d’édition après lancement]({{site.baseurl}}/post-launch_edits). Votre Canvas d’origine ne sera ni altéré ni supprimé.

Pour cloner votre Canvas, commencez par aller sur le tableau de bord Canvas. Ensuite, identifiez le Canvas que vous souhaitez copier dans le flux de travail Canvas Flow. Vous pouvez cloner des Canvas avec le statut **Ébauche**, **Actif** ou **Arrêté**. Cliquez sur <i class="fas fa-ellipsis-vertical"></i> **Plus d’actions** et sélectionnez **Cloner vers Canvas Flow**.

![][1]{: style="max-width:25%;"}

Ensuite, entrez le nom de votre nouveau Canvas et cliquez sur **Cloner vers Canvas Flow**. 

![][2]{: style="max-width:70%;"}

Vous disposez maintenant de deux versions pour votre Canvas : le Canvas originel et la version Canvas Flow. Votre Canvas originel aura toujours son statut d’origine et le Canvas cloné aura le statut **Ébauche**. Vous pouvez toujours accéder au Canvas originel, mais Braze recommande d’utiliser Canvas Flow pour continuer à concevoir vos Canvas.

Prenez note du fait que si vous clonez un Canvas actif, Braze continuera à envoyer les utilisateurs à travers le Canvas d’origine. Nous vous recommandons d’arrêter un Canvas avant de le cloner pour éviter d’envoyer des messages en double aux utilisateurs depuis les deux Canvas.

![Tableau de bord de Canvas avec deux Canvas répertoriés : Copie V2 de Canvas V1,et Canvas V1. La copie V2 du Canvas V1 comporte une icône qui indique qu’elle utilise le flux de travail Canvas Flow.][3]

Vous avez terminé de cloner votre Canvas dans le flux de travail Canvas Flow. Vous pouvez désormais continuer à générer vos Canvas avec cette mise à jour !

## Limitations

Lorsqu’un Canvas dispose de [branches]({{site.baseurl}}/user_guide/engagement_tools/canvas/create_a_canvas/branching/), les critères suivants doivent être remplis pour que le Canvas soit dupliqué dans Canvas Flow.
- Les conditions de délai de la branche sont les mêmes.
- La section d’audience n’est pas vide.
- Aucun événement d’exception n’est utilisé.
- La variante se divise en plusieurs étapes complètes (aucune étape complète ne se divise en plusieurs étapes).

### Exemples

Si un Canvas dispose de plusieurs étapes qui se rapportent à la variante (division au niveau de la variante), il ne peut pas être cloné dans Canvas Flow.

Cependant, si un Canvas dispose d’une division au niveau de la variante et que cette variante se divise en plusieurs étapes complètes selon les critères énumérés dans la section précédente, alors ce Canvas peut être cloné dans Canvas Flow.

![Exemple de Canvas qui se divise en deux étapes complètes depuis la variante.][4]{: style="max-width:50%;"}

Un autre exemple serait le suivant. Si un Canvas dispose d’une étape complète disposant d’événements d’exception et que cette étape complète utilise également les filtres de délais « dans » ou « pour le suivant », alors il ne peut pas être cloné dans Canvas Flow. Cependant, si une étape de Canvas utilise des événements d’exception ayant un autre type de délai, alors le Canvas peut être cloné dans Canvas Flow.

Pour plus d’informations concernant les différences entre l’éditeur Canvas d’origine et l’expérience Canvas Flow, consultez les [FAQ Canvas]({{site.baseurl}}/user_guide/engagement_tools/canvas/faqs/#what-are-the-main-differences-between-canvas-flow-and-the-original-canvas-editor).


[1]: {% image_buster /assets/img_archive/clone_to_v2_workflow.png %}
[2]: {% image_buster /assets/img_archive/clone_to_v2_modal.png %}
[3]: {% image_buster /assets/img_archive/clone_to_v2_dashboard.png %}
[4]: {% image_buster /assets/img_archive/clone_to_flow_variant.png %}
