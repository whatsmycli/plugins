# Example Plugin

A simple example plugin demonstrating platform detection and basic plugin structure.

## Usage

```bash
# Basic usage
whatsmy example

# With arguments (greet someone)
whatsmy example John
# Output: "Hello to you too, John!"

# Multiple arguments
whatsmy example foo bar
# Shows all arguments passed
```

## Example Output

```
==================================
  Example Plugin for whatsmycli  
==================================

Platform: Linux
System:   Linux 6.17.3-artix1-1

This is a template plugin!
Replace this code with your own implementation.

Tip: Return 0 for success, non-zero for errors.
```

## Source

[plugin-template](https://github.com/whatsmycli/plugin-template)

