
guard 'rake', :task => 'mrbtest' do
  watch(%r{^mrblib/(.+)\.rb$})
  watch(%r{^specs/(.+)\.rb$})
  watch(%r{^specs/libtest/libtest.dylib})
end

if RUBY_PLATFORM.include?('darwin')
  guard 'rake', task: 'specs/libtest/libtest.dylib' do
    watch(%r{^specs/libtest/libtest.c})
  end
  
else
  guard 'rake', task: 'specs/libtest/libtest.so' do
    watch(%r{^specs/libtest/libtest.c})
  end
  
end
