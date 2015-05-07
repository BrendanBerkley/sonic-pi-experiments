# Welcome to Sonic Pi v2.5

rel = 2
sleepy = 2

live_loop :chord_base do
  use_synth :tri
  play chord(:A3, :m7), release:rel
  sleep sleepy
  play chord(:C4), release:rel
  sleep sleepy
  play chord(:G3), release:rel
  sleep sleepy
  play chord(:D3), release:rel
  sleep sleepy

  play chord(:A3, :m7), release:rel
  sleep sleepy
  play chord(:C3), release:rel
  sleep sleepy
  play chord(:G3), release:rel
  sleep sleepy
  play chord(:D3), release:rel
  play :Fs4, release:rel
  sleep sleepy
end

live_loop :waterfall do
  use_synth :sine
  play_pattern_timed [:A4, :E4, :C4, :A4, :E4, :C4, :A4, :E4], 0.25
  sleep 0
  play_pattern_timed [:G4, :E4, :C4, :G4, :E4, :C4, :G4, :E4], 0.25
  sleep 0
  play_pattern_timed [:D5, :B4, :G4, :D5, :B4, :G4, :D5, :B4], 0.25
  sleep 0
  play_pattern_timed [:A4, :Fs4, :D4, :A4, :Fs4, :D4, :A4, :Fs4], 0.25
end