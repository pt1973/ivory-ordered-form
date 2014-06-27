# UPGRADE

### 1.0 to 1.1

The `Ivory\OrderedForm\Orderer\FormOrdererFactory` and `Ivory\OrderedForm\Orderer\FormFactory` has been removed as it
does not bring any value (except instantiate multiple form order which is not needed).

In order to only share a single instance of the form orderer, the
`Ivory\OrderedForm\ResolvedFormTypeFactory::$ordererFactory` has been renamed to
`Ivory\OrderedForm\ResolvedFormTypeFactory::$orderer` which now represents an
`Ivory\OrderedForm\Orderer\FormOrdererInterface`. Accordingly, the
`Ivory\OrderedForm\ResolvedFormTypeFactory::__construct` has been updated to take an optional
`Ivory\OrderedForm\Orderer\FormOrdererInterface`.