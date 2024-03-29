The Async API
=============

TronPy offers a standard synchronous API by default,
but also introduces an async client via `httpx <https://www.python-httpx.org/>`_.

The async client is ``AsyncTron``. It almost uses the same API as the synchronous client ``Tron``.

.. code-block:: python

  import asyncio

  from tronpy import AsyncTron
  from tronpy.keys import PrivateKey

          # > {'result': True, 'txid': 'edc2a625752b9c71fdd0d68117802860c6adb1a45c19fd631a41757fa334d72b'}
          print(await txn_ret.wait())
          # > {'id': 'edc2a625752b9c71fdd0d68117802860c6adb1a45c19fd631a41757fa334d72b', 'blockNumber': 10163821,
          # > 'blockTimeStamp': 1603368072000, 'contractResult': [''], 'receipt': {'net_usage': 283}}

  if __name__ == '__main__':
      asyncio.run(transfer())

API reference
-------------

.. autoclass:: tronpy.AsyncTron
   :members:

.. autoclass:: tronpy.async_tron.AsyncTrx
   :members:
