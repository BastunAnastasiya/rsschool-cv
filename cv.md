# Anastasiya Bastun

## Contacts 

| Social Media | Username                |
|--------------|-------------------------|
| Telegram     | @Bastun_Anastasia       |
| Email        | bastun.anastasiia@gmail |
| WhatsApp     | +7 (706) 411-75-87      |

## Summary

I've worked as an HR manager in IT for over 6 years. My strengths are communication, handling stress well, and being resourceful. During my job, I've implemented company policies, managed projects, and communicated with both employees and managers.

My main focus is keeping employees happy. To do this, I've improved how new hires adapt and perform.

My goal is to learn the basics of JavaScript, HTML, and CSS for further education and to switch careers later on.

## Skills

### Soft

- Communicability
- Responsiveness
- Empathy
- Involvement
- Attentiveness 
- Openness 
- Benevolence
- Stress tolerance
- Multitasking

### Hard

- Base HTML
    - blocks
    - semantic layout
    - SEO optimization
- Base CSS
    - flex
    - grid
    - media queries
    - transofmations
    - animations
- Base Javascript
    - types
    - functions
        - expression
        - declaration
        - arrow
        - IIFE
    - OOP
    - clojures
    - var vs let
    - const
    - DOM

### Code examples

```typescript
import { expect } from "chai";
import Token from "./token";
import { SignerWithAddress } from "@nomicfoundation/hardhat-ethers/signers";

describe("RebeccaCoin", () => {
  const token: Token = new Token();

  beforeEach(async () => {
    await token.deploy();
  });

  describe("Deployment", () => {
    it("should assign the total supply of the tokens to owner", async () => {
      const ownerBalance: bigint = (await token.balanceOf(
        token.owner?.address as string
      )) as bigint;

      expect(token.totalSupply).to.equal(ownerBalance);
    });
  });

  describe("Transactions", () => {
    it("should transfer tokens between accounts", async () => {
      const transferAmount: number = 50;

      await token.transfer(token.addr1 as SignerWithAddress, transferAmount);
      const addr1Balance: bigint = (await token.balanceOf(
        token.addr1?.address as string
      )) as bigint;
      expect(addr1Balance).to.equal(transferAmount);

      await token.transferAs(
        token.addr1 as SignerWithAddress,
        token.addr2 as SignerWithAddress,
        transferAmount
      );
      const addr2Balance: bigint = (await token.balanceOf(
        token.addr2?.address as string
      )) as bigint;
      expect(addr2Balance).to.equal(transferAmount);
    });

    it("should fail if sender doesn’t have enough tokens", async () => {
      const transferAmount: number = 1;
      const initialOwnerBalance: bigint = (await token.balanceOf(
        token.addr1?.address as string
      )) as bigint;

      expect(await token.balanceOf(token.addr1?.address as string)).to.equal(
        initialOwnerBalance
      );
    });

    it("should update balances after transfers", async () => {
      const transferAmount: bigint = 50n;
      const initialTransferAttempts: bigint = 2n;

      const initialOwnerBalance = (await token.balanceOf(
        token.owner?.address as string
      )) as bigint;

      await token.transfer(token.addr1 as SignerWithAddress, transferAmount);
      await token.transfer(token.addr2 as SignerWithAddress, transferAmount);

      const finalOwnerBalance: bigint = (await token.balanceOf(
        token.owner?.address as string
      )) as bigint;
      expect(finalOwnerBalance).to.equal(
        initialOwnerBalance - transferAmount * initialTransferAttempts
      );
    });
  });
});
```

## Work experience

Absent

## Education

- BSEU (2015-2019) Economics and management at the enterprise

## English level

- A2 
