    library ieee;
    use ieee.std_logic_1164.all;

    entity encoder4_2 is
    port(
       a : in std_logic_vector (3 downto 0);
       b : out std_logic_vector (1 downto 0) );
    
    end encoder4_2;

    architecture bhv of encoder4_2 is 
     begin
      process(a)
       begin
    
        if (a="0001") then b<="00";
        elsif(a="0010") then b<="01"; 
        elsif(a="0100") then b<="10";
        elsif(a="1000") then b<="11"; 
        else b<="ZZ";
        end if; 
      end process;
    end bhv;
    
    
