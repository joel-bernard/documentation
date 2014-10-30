Comment utiliser le plugin Jeditable
------------------------------------

Le plugin Jquery Jeditable est directement utilisable dans le html pour le bundle.

.. note::
    Pour activé l'initialisation du plugin, il suffit d'ajout la class CSS ``editable``

Attributs HTML :
================

==================================================   =========================================================================================================================
Attributs HTML disponibles                           Utilisation
==================================================   =========================================================================================================================
data-editable-load-url                               Url AJAX appeler pour l'affichage (getter).
data-editable-submit-url                             Url AJAX appeler pour la sauvegarde (setter).
data-editable-id                                     Nom de l'élément posté.
data-editable-type                                   Type de champ de formulaire à afficher lors de l'édition. Les valeurs possibles sont : ``text``, ``textarea``, ``select``.
data-editable-specific-callback                      Par défault : ``false``. Indique un callback spécifique pour le champ.
==============================================================================================================================================================================

Exemples :
==========

.. code-block:: html+jinja
    :linenos:

    <h1>code block example</h1>
    <span class="editable" data-editable-load-url="" data-editable-submit-url="" data-editable-id="" data-editable-type="">

