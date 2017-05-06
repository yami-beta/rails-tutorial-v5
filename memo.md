## ルーティング

### 名前付きルート

以下のようにルーティングを設定したとき、名前付きルートが利用できる。

```ruby
Rails.application.routes.draw do
  get '/sample', to: 'sample#index'
end
```

| 名前付きルート | URL                          | 利用例                            |
| :--:           | :--:                         | :--:                              |
| sample_url     | http://localhost:3000/sample | `redirect_to sample_path`         |
| sample_path    | /sample                      | `link_to "サンプル", sample_path` |

リダイレクトはURLが要求される仕様になっているため、`sample_url`を用いるのが良い。
しかし、大半のブラウザで`sample_path`を用いてもリダイレクトされる。

### 7.3.2

Rails 4からコントローラでStrong Parametersを用いることが推奨されている。

