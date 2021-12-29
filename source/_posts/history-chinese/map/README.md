Source: [中 國 歷 代 版 圖](https://www.chiculture.net/9001/map/index.htm)

Modifications:

- download swap image of main page
  ```fish
  cd image/images_index
  for file in *.gif
    set basename (string split -r . $file)[1]
    if string match -qvr '^\d\d_\d\d$' $basename
      echo skip $basename
      continue
    end
    wget https://www.chiculture.net/9001/map/image/images_index/"$basename"_01.gif
  end
  ```
- download new window htmls
  ```fish
  cd html
  for file in *.htm
    set basename (string split -r . $file)[1]
    if string match -qvr '^\d+$' $basename
      echo skip $basename
      continue
    end
    wget https://www.chiculture.net/9001/map/html/new_window_"$basename".htm
  end
  ```
- fix swap image of 唐 in main page
- convert to UTF-8
  `find . -name '*.htm*' -exec iconv -f big5 -t utf-8 {} -o {} \;`
  search and replace `charset=big5` with `charset=utf-8`
