constructor(
        address _libAddressManager,
        uint256 _maxTransactionGasLimit,
        uint256 _l2GasDiscountDivisor,
        uint256 _enqueueGasCost
    ) Lib_AddressResolver(_libAddressManager) {
        maxTransactionGasLimit = _maxTransactionGasLimit;
        l2GasDiscountDivisor = _l2GasDiscountDivisor;
        enqueueGasCost = _enqueueGasCost;
        enqueueL2GasPrepaid = _l2GasDiscountDivisor * _enqueueGasCost;
    }
