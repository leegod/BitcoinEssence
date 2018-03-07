BitcoinEssence integration/staging tree
================================

http://www.bitcoinessence.org

http://www.bitcoinessence.info

Copyright (c) 2009-2014 Bitcoin Developers

Copyright (c) 2011-2014 Litecoin Developers

Copyright (c) 2018 BitcoinEssence Developers 
(Lee Dong Hun)

What is BitcoinEssence?
----------------

BitcoinEssence is a lite version of Bitcoin using Scrypt as a Proof-Of-Work algorithm.
 - 15 second block targets 
 - Transaction speed is in few seconds
 - subsidy halves in 1,575,000 blocks (9 months)
 - 2,100,000,000 total coins
 - 500 coins per block
 - 25% of total coins were premined for develop, marketing cost, pre-sale, 75% of total coins is reserved for mining
 
 
The rest is the same as Bitcoin.  

For more information, as well as an immediately useable, binary version of
the BitcoinEssence client sofware, see http://www.bitcoinessence.org.

License
-------

BitcoinEssence is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the BitcoinEssence
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoinessence-project/bitcoinessence/tags) are created
regularly to indicate new official, stable release versions of BitcoinEssence.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./bitcoinessence-qt_test

