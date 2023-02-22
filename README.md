# test_audit_Mixbyte

Litra APP
=============

<YOUR_PROJECT_SHORT_OVERVIEW>
Понимание протокола было осложненно из-за отсутсвия логики, и хотя бы примерного понимания что делает протокол

All vulnerabilities discovered during the audit are classified based on their potential severity and have the following classification:
Severity | Description
-- | ---
Critical | Bugs leading to assets theft, fund access locking, or any other loss funds to be transferred to any party.
High     | Bugs that can trigger a contract failure. Further recovery is possible only by manual modification of the contract state or replacement.
Medium   | Bugs that can break the intended contract logic or expose it to DoS attacks, but do not cause direct loss funds.
Findings

Critical
Not found

High
Not found

Medium
<currentRate> в файле litra-contract/contracts/dao/LA.sol 
131 строка

<Description>
Rate считается от будущего к прошлому, т.е. сперва высчитывается рейт будущего периода, а потом этот рейт делится на какое-то число, чтобы получить рейт прошлого периода
и одновременно с этим Rate растет вместо того, чтобы уменьшаться с каждой эпохой как в mint

<Recommendation>
Вероятно один из RATE работает не правильно, стоит их синхронизировать

Low
Много непонятной логики, не понятно это БАГ или ФИЧА

