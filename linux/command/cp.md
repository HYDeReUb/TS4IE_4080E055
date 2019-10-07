用法：cp [選項]... [-T] 來源 目的地
  或：cp [選項]... 來源... 目錄
  或：cp [選項]... -t 目錄 來源...
Copy SOURCE to DEST, or multiple SOURCE(s) to DIRECTORY.

Mandatory arguments to long options are mandatory for short options too.
  -a, --archive                same as -dR --preserve=all
      --attributes-only        don't copy the file data, just the attributes
      --backup[=CONTROL]       make a backup of each existing destination file
  -b                           like --backup but does not accept an argument
      --copy-contents          copy contents of special files when recursive
  -d                           same as --no-dereference --preserve=links
  -f, --force                  if an existing destination file cannot be
                                 opened, remove it and try again (this option
                                 is ignored when the -n option is also used)
  -i, --interactive            prompt before overwrite (overrides a previous -n
                                  option)
  -H                           follow command-line symbolic links in SOURCE
  -l, --link                   hard link files instead of copying
  -L, --dereference            always follow symbolic links in SOURCE
  -n, --no-clobber             do not overwrite an existing file (overrides
                                 a previous -i option)
  -P, --no-dereference         never follow symbolic links in SOURCE
  -p                           same as --preserve=mode,ownership,timestamps
      --preserve[=ATTR_LIST]   preserve the specified attributes (default:
                                 mode,ownership,timestamps), if possible
                                 additional attributes: context, links, xattr,
                                 all
      --no-preserve=ATTR_LIST  don't preserve the specified attributes
      --parents                use full source file name under DIRECTORY
  -R, -r, --recursive          copy directories recursively
      --reflink[=WHEN]         control clone/CoW copies. See below
      --remove-destination     remove each existing destination file before
                                 attempting to open it (contrast with --force)
      --sparse=WHEN            control creation of sparse files. See below
      --strip-trailing-slashes  remove any trailing slashes from each SOURCE
                                 argument
  -s, --symbolic-link          只建立符號鏈結而不是複製檔案
  -S, --suffix=後置字串        自行指定備份檔的 <後置字串>
  -t, --target-directory=目錄  將所有 <來源> 檔案/目錄複製至指定的 <目錄>
  -T, --no-target-directory    將 <目的地> 看作普通檔案處理
  -u, --update                 只在 <來源> 檔案比目的地檔案新，
                               或目的地檔案不存在時才進行複製
  -v, --verbose                詳細顯示進行的步驟
  -x, --one-file-system        不會跨越檔案系統進行操作
  -Z                           set SELinux security context of destination
                                 file to default type
      --context[=CTX]          like -Z, or if CTX is specified then set the
                                 SELinux or SMACK security context to CTX
      --help     顯示此求助說明並離開
      --version  顯示版本資訊並離開

By default, sparse SOURCE files are detected by a crude heuristic and the
corresponding DEST file is made sparse as well.  That is the behavior
selected by --sparse=auto.  Specify --sparse=always to create a sparse DEST
file whenever the SOURCE file contains a long enough sequence of zero bytes.
Use --sparse=never to inhibit creation of sparse files.

When --reflink[=always] is specified, perform a lightweight copy, where the
data blocks are copied only when modified.  If this is not possible the copy
fails, or if --reflink=auto is specified, fall back to a standard copy.
Use --reflink=never to ensure a standard copy is performed.

The backup suffix is '~', unless set with --suffix or SIMPLE_BACKUP_SUFFIX.
The version control method may be selected via the --backup option or through
the VERSION_CONTROL environment variable.  Here are the values:

  none, off       不會進行備份 (即使使用了 --backup 選項也不會)
  numbered, t     備份檔會加上數字
  existing, nil   若有數字的備份檔已經存在則使用數字，否則使用普通方式備份
  simple, never   永遠使用普通方式備份

有一個特別情況：如果同時指定 --force 和 --backup 選項，而且 <來源> 和
<目的地> 是同一個已存在的普通檔案的話，cp 會將 <來源> 檔案備份。

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report cp translation bugs to <https://translationproject.org/team/>
Full documentation at: <https://www.gnu.org/software/coreutils/cp>
or available locally via: info '(coreutils) cp invocation'
