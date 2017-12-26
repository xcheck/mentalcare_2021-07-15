#### procmailrc

| read | pick ^preprocessor | workflow | compile ^compiler | only |
| :--: | :--: | :--: | :--: | :--: |
| | C | _-eq as first compile action_ | c | |
| | H | | h | pipe incl. header |
| | B | | b | pipe incl. body |
