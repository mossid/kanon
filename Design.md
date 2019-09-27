# Kanon

DAO framework for conscious coordination

## Principles

The mechanism of the organization should be written down in language, as precise as possible.

## Architecture

Kanon is based on object capability principle.

An `org` is composed of multiple `logic`s. A `logic` is a stateful entity that can interact with outside world.

`Logic`s can be invoked by either function call or event. Function call can be happen only by another logic or itself in the same `org`. Event can be used to interact with the real world or other `org`s. 

`Permission`s are linear assets tied to `logic`s. "Linear" means that the `permission`s cannot be copied(although they can be deleted). `Logic`s can define which `permission`s will be generated and transferred to the creator. The `permission`s will be tied on a specific functions in the `logic`s, in way that entities not holding the `permission` cannot access on the functions. The primitive operations will include some permission combinators, and more complex permission combination can be done with future Jessie integration.

Primitive `logic`s are provided by the runtime, including:
- Voting: create 

Here are some of the example `logic`s.

- Dispatcher: receives events from the real world or other `org`s, dispatches it to appropriate `logic`s.
- CodeRouter: routes internal function call to external code reference
- Accounter: accumulates funds and send it with predefined conditionals
- Vote: invokes a function only if the majority of the voters agreed on to do.
- Sudo: has master permission on any `logic`s inside the `org`.

All of the `logic` are amendable. When a `logic` is created, the master permission on the `logic`, including the amending right, is given to the creator. The creator, which can be another `logic` or a real world entity, can use the permission to amend the `logic` when needed. For personal purpose it can be a high secure multisig wallet as the creator and a rate-limited simple wallet as a `logic` - the creator, when needed, amend the mechanics of the simple wallet and withdraw all the remaining funds. For organizational purpose, it can be token holder's vote and the amended voting rule. The original voting `logic` have to give its permission to access on funds, amending rights, etc. to the new voting `logic` to make it work, so once it transferred the permissions to the new `logic` it is no longer able to make any rule changes anymore.

## Components

### Primitive Operations

#### Accounts

- CreateAccount
- 

#### Permissions

#### Decision Making

#### 

### Jessie Integration

