用法：mv [選項]... [-T] 來源 目的地
  或：mv [選項]... 來源... 目錄
  或：mv [選項]... -t 目錄 來源...
Rename SOURCE to DEST, or move SOURCE(s) to DIRECTORY.

Mandatory arguments to long options are mandatory for short options too.
      --backup[=CONTROL]       make a backup of each existing destination file
  -b                           like --backup but does not accept an argument
  -f, --force                  do not prompt before overwriting
  -i, --interactive            prompt before overwrite
  -n, --no-clobber             do not overwrite an existing file
If you specify more than one of -i, -f, -n, only the final one takes effect.
      --strip-trailing-slashes  remove any trailing slashes from each SOURCE
                                 argument
  -S, --suffix=SUFFIX          override the usual backup suffix
  -t, --target-directory=DIRECTORY  move all SOURCE arguments into DIRECTORY
  -T, --no-target-directory    treat DEST as a normal file
  -u, --update                 move only when the SOURCE file is newer
                                 than the destination file or when the
                                 destination file is missing
  -v, --verbose                explain what is being done
  -Z, --context                set SELinux security context of destination
                                 file to default type
      --help     顯示此求助說明並離開
      --version  顯示版本資訊並離開

The backup suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.
The version control method may be selected via the --backup option or through
the VERSION_CONTROL environment variable.  Here are the values:

  none, off       不會進行備份 (即使使用了 --backup 選項也不會)
  numbered, t     備份檔會加上數字
  existing, nil   若有數字的備份檔已經存在則使用數字，否則使用普通方式備份
  simple, never   永遠使用普通方式備份

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report mv translation bugs to <https://translationproject.org/team/>
Full documentation at: <https://www.gnu.org/software/coreutils/mv>
or available locally via: info '(coreutils) mv invocation'
