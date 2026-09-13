# Anatomica Reference

Anatomica is a tiny, text-first notation for describing the anatomy of software products. It models **Screens, Components, Actions, States, and Flows** so teams can make product structure visible before pixels or code.

Canonical source: https://github.com/drewbarontini/anatomica

## Grammar

```text
[Screen]::Component.SubComponent@state.action() => [dest] | ::Component | .action() | @state
```

## Core notation

```text
[Screen]                      # screen
[Screen@state]                # screen in a state
[Screen]::Component           # component on a screen
::Component.SubComponent      # nested component
::Component@state             # component in a state
::Component.action()          # action on a component
.action() => [Screen]         # navigate to a screen
.action() => ::Component      # focus/open a component
.action() => .action()        # chain to another action
.action() => @state           # transition to a state
// comment                    # commentary above a line
```

## Indented style

Use indentation to show hierarchy and reduce repetition.

```text
[Inbox]
  ::MessageList
    ::MessageListItem
      .open() => [MessageDetail]
      .archive()
  ::ComposeButton
    .click() => ::NewMessageModal@open
```

## Conventions

- **Screens** are top-level product surfaces or contexts.
- **Components** are structural parts of a screen or flow.
- **Actions** are user or system behaviors tied to a component.
- **States** are rendering or behavioral conditions.
- **Flows** are directed transitions between screens, components, actions, or states.
- Model modals as components with explicit states such as `@open` and `@closed`.
- Model lists and their items as distinct components when their behaviors differ.
- Use comments sparingly to capture context that notation alone cannot express.
- Keep event-style naming stable enough that the map can align with analytics when useful.
