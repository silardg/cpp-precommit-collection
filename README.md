# cpp-precommit-collection

This library is ment to be included into future C++ projects that are versioned on github.

## Main features
- using [pre-commit hook](https://pre-commit.com/) 
- hooks:
  - [clang-format](https://clang.llvm.org/)
  - [cppcheck](https://github.com/danmar/cppcheck)
  - [cpplint](https://github.com/cpplint/cpplint)
- custom clang-format formatting based on Microsoft

### clang-format
- Documentation: [link](https://clang.llvm.org/docs/ClangFormat.html)
- Custom commands used: `--style=file`
- Command used to format all the files in the current directory: `clang-format -style=file -i *`

### cppcheck
- Documentation: [link](https://cppcheck.sourceforge.io/manual.html)
- Custom commands used: `--language=c++ --enable=performance,unusedFunction --std=c++11`

### cpplint
- Documentation: [link](https://help.sider.review/tools/cplusplus/cpplint/)
  - it's following [Googles](https://google.github.io/styleguide/cppguide.html) style
- Custom commands used: `--filter=-build/include_order,-build/include_subdir,-whitespace/indent,-whitespace/braces,-whitespace/line_length,-readability/casting,-whitespace/parens --extensions=hpp,cpp,c,h`

## Files
- .pre-commit-config.yaml
  - contains every hook and the custom commands
- .clang-format
  - custom format based on Microsoft
- defaults.cfg
  - default formating
