# Changelog

## 2.0.0 (2017-10-08)
* Removed `Mockery.Heritage`
  * Global mocks will be handled without macros by pure elixir modules.
  * Some new restrictions have been added for global mock modules (see global
    mock section in README)
* Changed `Mockery.mock/3` when value is function (dynamic mock)
  * `[function_name: arity]` syntax remains unchanged
  * `:function_name` syntax will raise error
* Changed `Mockery.of/2` output
  * run `mix compile --force` when upgrading from Mockery 1.x.x

## 1.4.0 (2017-10-02)
* `Mockery.mock/2` and `Mockery.mock/3` are now chainable

## 1.3.1 (2017-09-21)
* Minor format fix in `Mockery.History` failure messages

## 1.3.0 (2017-09-15)
* Added string version for `Mockery.of/2` (now recommended)
* Fixed mocking of erlang modules

## 1.2.0 (2017-09-13)
* Introduced `Mockery.History`

## 1.1.1 (2017-09-05)
* More descriptive errors (when args are not list) for:
  * `Mockery.Assertions.assert_called/3`
  * `Mockery.Assertions.refute_called/3`
  * `Mockery.Assertions.assert_called/4`
  * `Mockery.Assertions.refute_called/4`
* Removed unnecessary `Elixir.` namespace from module names in error messages

## 1.1.0 (2017-08-07)
* Added `Mockery.mock/2` (`Mockery.mock/3` value defaults to `:mocked`)
* Added `Mockery.Assertions.assert_called/4` macro
* Added `Mockery.Assertions.refute_called/4` macro

## 1.0.1 (2017-08-02)
* Fixed issue when mocking with `nil` or `false`

## 1.0.0 (2017-07-30)
* Added `use Mockery` for importing both `Mockery` and `Mockery.Assertions`
* Added `Mockery.Assertions.refute_called/2` and `Mockery.Assertions.refute_called/3`
* Loosen elixir version requirement from `~> 1.3` to `~> 1.1`
