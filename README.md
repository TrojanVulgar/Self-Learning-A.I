"# Self-Learning-A.I" 
AUTHOR CESAR VERSATTI


public String transform(String str)
    {
        //make sure string is not null
        if(str == null){
            return null;
        }

        //make string readable for system
        char[] replacements = ("!?;:.,\"'*@€|~{}[]()\n").toCharArray();
        for(char c: replacements){
            String rep = String.valueOf(c);
            if(str.toLowerCase().contains(rep.toLowerCase())){
                try{
                    str = str.replaceAll(rep, "");
                }catch(Exception e){}
            }
        }

        return str.trim();
    }

    &&

    Consider:

/*transform a string into something the program can read*/
private static String transform(String s) {
    return s.toLowerCase()
            .replace("?", "")
            .replace(".", "")
            .replace("!", "")
            .replace(",", "")
            .replace("_", "")
            .replace("~", "")
            .replace("`", "")
            .replace("'", "")
            .replace("\"", "")
            .replace("\"", "")
            .replace("\\", "")
            .replace(":", "")
            .replace(";", "")
            .replace("the", " ")
            .replace("teh", " ")
            .replace("how do", "how can")
            .replace("re", "")
            .replace(" a ", " ")
            .replace("is", "")
            .replace("has", "")
            .replace("get to", "go to")
            .replaceAll("\\Bs\\b", "")
            .replaceAll(" {2}?", "")
            .trim();
}