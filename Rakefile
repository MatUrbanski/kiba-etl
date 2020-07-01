require 'kiba'
require_relative 'common'

task :kiba_run do
  puts "The job is running..."

  Kiba.run(
    Kiba.parse do
      ##############################################################
      source SourceCSV, filename: 'phone.csv'

      transform TransformClean, field: 'number'
      transform TransformDropFake, field: 'number'

      destination DestinationCSV, filename: 'numbers-cleaned.csv'
      ##############################################################
    end
  )

  puts "...The job is finished"
end
