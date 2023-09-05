# Ruby Gym: Secret Encoder

Write a program that ingests a secret message and "encodes" the message by replacing vowels with other characters

Here is our secret code, don't tell anyone: 
    ```
    a = 1, e = 2, i = 3, o = 4, u = 5
    ```

Your program should print the encoded message.

Make sure each of these the `secret` strings below output the correct encoded response, then get the tests to pass.

```ruby
secret = [
  "I have a secret to share",
  "Is this secure enough for my PASSWORD?",
  "we should be more clever"
].sample
pp secret
# write your program below
```
{: .repl #secret_encoder title="Secret Encoder" readonly_lines="[1,2,3,4,5,6,7]"}


```ruby
describe "Secret Encoder" do
  it "prints '3 n22d t4 b2 m4r2 s2cr2t', when the input is 'I need to be more secret'" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return("I need to be more secret")
    expect { require_relative(path) }.to output(/3 n22d t4 b2 m4r2 s2cr2t/i).to_stdout
  end
end
```
{: .repl-test #secret_encoder_test_1 for="secret_encoder" title="Secret Encoder prints '3 n22d t4 b2 m4r2 s2cr2t', when the input is 'I need to be more secret'" points="1"}

```ruby
describe "Secret Encoder" do
  it "prints 'D4n't t2ll 1ny4n2 45r c4d2', when the input is 'Don't tell anyone our code'" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return("Don't tell anyone our code")
    expect { require_relative(path) }.to output(/D4n't t2ll 1ny4n2 45r c4d2/i).to_stdout
  end
end
```
{: .repl-test #secret_encoder_test_2 for="secret_encoder" title="Secret Encoder prints 'D4n't t2ll 1ny4n2 45r c4d2', when the input is 'Don't tell anyone our code'" points="1"}
