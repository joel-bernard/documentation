Comment utiliser le plugin Jeditable
------------------------------------

Le plugin Jquery Jeditable est directement utilisable dans le html pour le bundle.

.. note:: Pour activé l'initialisation du plugin, il suffit d'ajout la class CSS ``editable``

Attributs HTML :
================

==================================================   =========================================================================================================================
Attributs HTML disponibles                           Utilisation
==================================================   =========================================================================================================================
data-editable-load-url                               Url AJAX appeler pour l'affichage (getter).
data-editable-submit-url                             Url AJAX appeler pour la sauvegarde (setter).
data-editable-id                                     Nom de l'élément posté.
data-editable-type                                   Type de champ de formulaire à afficher lors de l'édition. Les valeurs possibles sont : ``text``, ``textarea``, ``select``
data-editable-specific-callback                      Par défault : ``false``. Indique un callback spécifique pour le champ. Voir `documentation <http://www.appelsiini.net/projects/jeditable>`_
==================================================   =========================================================================================================================

Exemples :
==========

Utilisation sans callback spécifique :

.. code-block:: html

    <span
        class="editable"
        data-editable-load-url=""
        data-editable-submit-url=""
        data-editable-id=""
        data-editable-type=""
    >
        my-value
    </span>

Avec callback spécifique :

Partie HTML :

.. code-block:: html

    <span
        class="editable"
        data-editable-load-url=""
        data-editable-submit-url=""
        data-editable-id=""
        data-editable-type=""
        data-editable-specific-callback=""
    >
        my-value
    </span>

Partie Js :

 .. code-block:: js

     window.AppTool.UI.jeditable($(this), function (value) {
            if ($(this).data('editable-reload') === 'true') {
                window.location.reload();
            } else {
                var response = $.parseJSON(value);
                $(this).attr('data-editable-load-url', Routing.generate('lecadmin_tva_get', {id: response.id}));
                $(this).html(response.data);
            }
     });
