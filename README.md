# latin
Topic Modeling of Latin Texts Your Health

Config Instructions

Required Parameters
 Source: a string representing the file name from which you want to draw your data
 Iterations: an integer representing the number of iterations you want to run
 Topics: an integer representing the number of topics you want to sort words into
 Output Name: a string representing the file name you want this model's output files to have

Stopword Options*
 Upper Limit: either a decimal value between 0 and 1 describing the percentage (or greater) of documents a word must
 appear in if it is to be tagged as a stopword OR “off” if you do not wish to use this feature
 Lower Limit: either a decimal value between 0 and 1 describing the percentage (or fewer) of documents a word must
 appear in if it is to be tagged as a stopword OR “off” if you do not wish to use this feature
 Whitelist: either a list of words to whitelist OR “off” if you do not wish to use this feature
 Blacklist: either a list of words to blacklist OR “off” if you do not wish to use this feature

Chunking Options
Note: only one of these methods may be used at one time; if a config file refers to more than one,
only the first will be used.
 Number of Documents: an integer representing the number of documents a text should be divided into OR “off” if you
 are using a different chunking method
 Length of Documents: an integer representing the number of words to make each document OR “off” if you are using a
 different chunking method
 Split String: a string representing the sequence of characters that separates documents from one another OR “off” if
 you are using a different chunking method

Hyperparameters
 Alpha: a decimal value between 0 and 1 representing how similar topics should be to each other in topic makeup
 Beta: a decimal value between 0 and 1 representing how similar topics should be to each other in word makeup

*Here are good default stopword lists for English and Latin (taken from stopword lists at www.perseus.tufts.edu)
You can just copy these arrays into the blacklist in the configuration file

English: ["a", "a's", "able", "about", "above", "according", "accordingly", "across", "actually", "after", "afterwards",
          "again", "against", "ain't", "all", "allow", "allows", "almost", "alone", "along", "already", "also",
          "although", "always", "am", "among", "amongst", "an", "and", "another", "any", "anybody", "anyhow", "anyone",
          "anything", "anyway", "anyways", "anywhere", "apart", "appear", "appreciate", "appropriate", "are", "aren't",
          "around", "as", "aside", "ask", "asking", "associated", "at", "available", "away", "awfully", "b", "be",
          "became", "because", "become", "becomes", "becoming", "been", "before", "beforehand", "behind", "being",
          "believe", "below", "beside", "besides", "best", "better", "between", "beyond", "both", "brief", "but", "by",
          "c", "c'mon", "c's", "came", "can", "can't", "cannot", "cant", "cause", "causes", "certain", "certainly",
          "changes", "clearly", "co", "com", "come", "comes", "concerning", "consequently", "consider", "considering",
          "contain", "containing", "contains", "corresponding", "could", "couldn't", "course", "currently", "d",
          "definitely", "described", "despite", "did", "didn't", "different", "do", "does", "doesn't", "doing", "don't",
          "done", "down", "downwards", "during", "e", "each", "edu", "eg", "eight", "either", "else", "elsewhere",
          "enough", "entirely", "especially", "et", "etc", "even", "ever", "every", "everybody", "everyone",
          "everything", "everywhere", "ex", "exactly", "example", "except", "f", "far", "few", "fifth", "first", "five",
          "followed", "following", "follows", "for", "former", "formerly", "forth", "four", "from", "further",
          "furthermore", "g", "get", "gets", "getting", "given", "gives", "go", "goes", "going", "gone", "got",
          "gotten", "greetings", "h", "had", "hadn't", "happens", "hardly", "has", "hasn't", "have", "haven't",
          "having", "he", "he's", "hello", "help", "hence", "her", "here", "here's", "hereafter", "hereby", "herein",
          "hereupon", "hers", "herself", "hi", "him", "himself", "his", "hither", "hopefully", "how", "howbeit",
          "however", "i", "i'd", "i'll", "i'm", "i've", "ie", "if", "ignored", "immediate", "in", "inasmuch", "inc",
          "indeed", "indicate", "indicated", "indicates", "inner", "insofar", "instead", "into", "inward", "is",
          "isn't", "it", "it'd", "it'll", "it's", "its", "itself", "j", "just", "k", "keep", "keeps", "kept", "know",
          "known", "knows", "l", "last", "lately", "later", "latter", "latterly", "least", "less", "lest", "let",
          "let's", "like", "liked", "likely", "little", "look", "looking", "looks", "ltd", "m", "mainly", "many", "may",
          "maybe", "me", "mean", "meanwhile", "merely", "might", "more", "moreover", "most", "mostly", "much", "must",
          "my", "myself", "n", "name", "namely", "nd", "near", "nearly", "necessary", "need", "needs", "neither",
          "never", "nevertheless", "new", "next", "nine", "no", "nobody", "non", "none", "noone", "nor", "normally",
          "not", "nothing", "novel", "now", "nowhere", "o", "obviously", "of", "off", "often", "oh", "ok", "okay",
          "old", "on", "once", "one", "ones", "only", "onto", "or", "other", "others", "otherwise", "ought", "our",
          "ours", "ourselves", "out", "outside", "over", "overall", "own", "p", "particular", "particularly", "per",
          "perhaps", "placed", "please", "plus", "possible", "presumably", "probably", "provides", "q", "que", "quite",
          "qv", "r", "rather", "rd", "re", "really", "reasonably", "regarding", "regardless", "regards", "relatively",
          "respectively", "right", "s", "said", "same", "saw", "say", "saying", "says", "second", "secondly", "see",
          "seeing", "seem", "seemed", "seeming", "seems", "seen", "self", "selves", "sensible", "sent", "serious",
          "seriously", "seven", "several", "shall", "she", "should", "shouldn't", "since", "six", "so", "some",
          "somebody", "somehow", "someone", "something", "sometime", "sometimes", "somewhat", "somewhere", "soon",
          "sorry", "specified", "specify", "specifying", "still", "sub", "such", "sup", "sure", "t", "t's", "take",
          "taken", "tell", "tends", "th", "than", "thank", "thanks", "thanx", "that", "that's", "thats", "the", "their",
          "theirs", "them", "themselves", "then", "thence", "there", "there's", "thereafter", "thereby", "therefore",
          "therein", "theres", "thereupon", "these", "they", "they'd", "they'll", "they're", "they've", "think",
          "third", "this", "thorough", "thoroughly", "those", "though", "three", "through", "throughout", "thru",
          "thus", "to", "together", "too", "took", "toward", "towards", "tried", "tries", "truly", "try", "trying",
          "twice", "two", "u", "un", "under", "unfortunately", "unless", "unlikely", "until", "unto", "up", "upon",
          "us", "use", "used", "useful", "uses", "using", "usually", "uucp", "v", "value", "various", "very", "via",
          "viz", "vs", "w", "want", "wants", "was", "wasn't", "way", "we", "we'd", "we'll", "we're", "we've", "welcome",
          "well", "went", "were", "weren't", "what", "what's", "whatever", "when", "whence", "whenever", "where",
          "where's", "whereafter", "whereas", "whereby", "wherein", "whereupon", "wherever", "whether", "which",
          "while", "whilst", "whither", "who", "who's", "whoever", "whole", "whom", "whose", "why", "will", "willing",
          "wish", "with", "within", "without", "won't", "wonder", "would", "wouldn't", "x", "y", "yes", "yet", "you",
          "you'd", "you'll", "you're", "you've", "your", "yours", "yourself", "yourselves", "z", "zero"]

Latin: ["ab", "ac", "ad", "adhic", "aliqui", "aliquis", "an", "ante", "apud", "at", "atque", "aut", "autem", "cum",
        "cur", "de", "deinde", "dum", "ego", "enim", "ergo", "es", "est", "et", "etiam", "etsi", "ex", "fio", "haud",
        "hic", "iam", "idem", "igitur", "ille", "in", "infra", "inter", "interim", "ipse", "is", "ita", "magis", "modo",
        "mox", "nam", "ne", "nec", "necque", "neque", "nisi", "non", "nos", "o", "ob", "per", "possum", "post", "pro",
        "quae", "quam", "quare", "qui", "quia", "quicumque", "quidem", "quilibet", "quis", "quisnam", "quisquam",
        "quisque", "quisquis", "quo", "quoniam", "sed", "si", "sic", "sive", "sub", "sui", "sum", "super", "suus",
        "tam", "tamen", "trans", "tu", "tum", "ubi", "uel", "uero", "unus", "ut"]