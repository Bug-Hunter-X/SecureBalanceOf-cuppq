# Reentrancy Vulnerability in balanceOf Function

This repository demonstrates a reentrancy vulnerability in a simple ERC20 token contract's `balanceOf` function.  The vulnerability allows an attacker to manipulate the balance reported by the contract.

## Vulnerability Details

The `balanceOf` function directly returns the balance from storage.  This is susceptible to reentrancy if an attacker's contract calls `balanceOf` as part of a reentrant attack.

## Mitigation

The solution demonstrates how to fix this by using a non-reentrant approach, ensuring that balance cannot be manipulated during the execution.