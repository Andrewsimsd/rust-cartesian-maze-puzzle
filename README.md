# 🧭 cartesian-maze-puzzle

[![Crates.io](https://img.shields.io/crates/v/cartesian-maze-puzzle.svg)](https://crates.io/crates/cartesian-maze-puzzle)
[![Docs.rs](https://docs.rs/cartesian-maze-puzzle/badge.svg)](https://docs.rs/cartesian-maze-puzzle)

A minimal, efficient, and fun procedural maze generation library written in Rust 🦀. Generate perfect mazes (no loops, no isolated sections), navigate them programmatically, and use them for puzzles, games, AI pathfinding, or teaching algorithms.

---

## 🚀 Features

- Generates perfect mazes using randomized depth-first search (DFS)
- Easy-to-use API to move through the maze
- Fully deterministic size and layout
- Lightweight with zero external dependencies beyond `rand`
- Built-in unit tests
- Suitable for CLI, GUI, or game integration

---

## 📦 Installation

Add the following to your `Cargo.toml`:

```toml
[dependencies]
cartesian-maze-puzzle = "0.1"
```

---

## 🧱 Example

```rust
use cartesian_maze_puzzle::{Maze, Direction};

fn main() {
    let mut maze = Maze::new(5, 5);

    println!("Starting at: {:?}", maze.player);
    
    // Try moving east
    if maze.try_move(Direction::East) {
        println!("Moved to: {:?}", maze.player);
    } else {
        println!("Hit a wall!");
    }

    // Check if you've reached the end
    if maze.is_at_end() {
        println!("You solved the maze!");
    }
}
```

---

## 🧪 Tests

Run unit tests with:

```bash
cargo test
```

Tests verify:

- Valid movement and boundary constraints
- All cells are reachable
- Player position is correctly updated
- Maze is fully connected (i.e., perfect maze)

---

## 📚 Documentation

The full API is available on [docs.rs](https://docs.rs/cartesian-maze-puzzle).

---

## 🤔 Why "Cartesian"?

Because the maze operates on a classic Cartesian coordinate grid where `(0, 0)` is the top-left corner. It's simple, intuitive, and easy to visualize or integrate into grid-based games.

---

## 📂 Folder Structure Suggestion

```
src/
├── lib.rs          # Maze logic
├── main.rs         # (Optional) CLI or demo interface
tests/
├── integration.rs  # Integration tests
```

---

## 📜 License

Licensed under either of:

- Apache License, Version 2.0
- MIT license

See [LICENSE](LICENSE) for more information.

---

## ✨ Contribution

Contributions welcome! Feel free to open issues or PRs for:

- Bug fixes
- Maze solving/pathfinding algorithms
- CLI game implementation
- Visualization features (ASCII or graphics)

---

## ❤️ Acknowledgments

Thanks to the Rust community and all contributors to the `rand` crate!

---

Made with 🧩 by [Andrew Sims](https://github.com/andrewsimsd)

