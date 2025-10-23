# frozen_string_literal: true

require "rake"

task default: :test

desc "Build the site."
task :build do
  sh "jekyll", "build"
end

desc "Run HTMLProofer to validate the HTML output."
task test: :build do
  require "html-proofer"
  HTMLProofer.check_directory(
    "./_site",
    parallel:            { in_threads: 4 },
    favicon:             true,
    ignore_status_codes: [0, 403],
    check_favicon:       true,
    check_opengraph:     true,
    check_html:          true,
    check_img_http:      true,
    enforce_https:       true,
    ignore_urls:         [
      "/issues/new",
      "https://podcasts.apple.com/gb/podcast/minimum-viable-management/id1845078315",
    ],
    cache:               {
      timeframe: {
        external: "1d",
        internal: "1h",
      },
    },
  ).run
end
