fireapp-data-demo
=================

You can easily load YAML files in `view_helpers.rb` in Fire.app, and use it like http://middlemanapp.com/advanced/local-data/

The `view_helpers.rb` contains this 5 lines only:

```
module ViewHelpers
  def data
    d||=YAML.load_file(File.join(File.dirname(__FILE__), 'data.yml'))
    return d
  end
end
```
