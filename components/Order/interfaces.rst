Interfaces
==========

Model Interfaces
----------------

.. _component_order_model_adjustment-interface:

AdjustmentInterface
~~~~~~~~~~~~~~~~~~~

This interface should be implemented by model representing a single Adjustment.

.. note::
    This interface extends the :ref:`component_resource_model_timestampable-interface` and the :ref:`component_originator_model_origin-aware-interface` |br|
    For more detailed information go to `Sylius API AdjustmentInterface`_.

.. _Sylius API AdjustmentInterface: http://api.sylius.org/Sylius/Component/Order/Model/AdjustmentInterface.html

.. _component_order_model_adjustable-interface:

AdjustableInterface
~~~~~~~~~~~~~~~~~~~

This interface provides basic operations for adjustment management.
Use this interface if you want to make a model adjustable.

For example following models implement this interface:
    * :ref:`component_resource_model_order`
    * :ref:`component_resource_model_order-item`

.. note::
    For more detailed information go to `Sylius API AdjustableInterface`_.

.. _Sylius API AdjustableInterface: http://api.sylius.org/Sylius/Component/Order/Model/AdjustableInterface.html

.. _component_order_model_comment-interface:

CommentInterface
~~~~~~~~~~~~~~~~

This interface should be implemented by model representing a single Comment.

.. note::
    This interface extends the :ref:`sylius_component_resource_model_timestampable-interface` |br|
    For more detailed information go to `Sylius API CommentInterface`_.

.. _Sylius API CommentInterface: http://api.sylius.org/Sylius/Component/Order/Model/CommentInterface.html

.. _component_order_model_comment-aware-interface:

CommentAwareInterface
~~~~~~~~~~~~~~~~~~~~~

This interface provides basic operations for comments management.
If you want to have comments in your model just implement this interface.

.. note::
    For more detailed information go to `Sylius API CommentAwareInterface`_.

.. _Sylius API CommentAwareInterface: http://api.sylius.org/Sylius/Component/Order/Model/CommentAwareInterface.html

.. _component_order_model_order-interface:

OrderInterface
~~~~~~~~~~~~~~

This interface should be implemented by model representing a single Order.

.. hint::
    It also contains the default :doc:`/components/Order/order_states`.

.. note::
    This interface extends :ref:`component_resource_model_timestampable-interface`, :ref:`component_resource_model_timestampable-interface`,
    :ref:`component_order_model_adjustable-interface`, :ref:`component_order_model_comment-aware-interface`,
    :ref:`component_resource_model_soft-deletable-interface` and :ref:`component_sequence_model_sequence-subject-interface`. |br|
    For more detailed information go to `Sylius API OrderInterface`_.

.. _Sylius API OrderInterface: http://api.sylius.org/Sylius/Component/Order/Model/OrderInterface.html

.. _component_order_model_order-aware-interface:

OrderAwareInterface
~~~~~~~~~~~~~~~~~~~

This interface provides basic operations for order management.
If you want to have orders in your model just implement this interface.

.. note::
    For more detailed information go to `Sylius API OrderAwareInterface`_.

.. _Sylius API OrderAwareInterface: http://api.sylius.org/Sylius/Component/Order/Model/OrderAwareInterface.html

.. _component_order_model_order-item-interface:

OrderItemInterface
~~~~~~~~~~~~~~~~~~

This interface should be implemented by model representing a single OrderItem.

.. note::
    This interface extends the :ref:`component_order_model_order-aware-interface` and the :ref:`component_order_model_adjustable-interface`, |br|
    For more detailed information go to `Sylius API OrderItemInterface`_.

.. _Sylius API OrderItemInterface: http://api.sylius.org/Sylius/Component/Order/Model/OrderItemInterface.html

Services Interfaces
-------------------

.. _component_order_repository_order-repository-interface:

OrderRepositoryInterface
~~~~~~~~~~~~~~~~~~~~~~~~

In order to decouple from storage that provides recently completed orders or check if given order's number is already used,
you should create repository class which implements this interface.

.. note::
    This interface extends the :ref:`component_resource_repository_repository-interface` and
    the :ref:`component_sequence_repository_hash-subject-repository-interface`. |br|
    For more detailed information about the interface go to `Sylius API OrderRepositoryInterface`_.
    
.. _Sylius API OrderRepositoryInterface: http://api.sylius.org/Sylius/Component/Order/Repository/OrderRepositoryInterface.html

