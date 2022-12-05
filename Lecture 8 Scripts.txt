##################################################
#
# This does not run on its own, but requires that you have 
#   already created a 2x2 table called "tab" with counts 
#   for X=true outcome and Y=test result

###########################################################
# Marginal proportions in each direction

(prev.props = rowSums(tab)/sum(tab))
(test.props = colSums(tab)/sum(tab))

# Compute test sensitivity and specificity from sample
#   These are just conditional probabilities given true 
#   (population) status

prop.table(x=tab, margin="truth")

# Compute positive and negative predictive values
#   These are just conditional probabilities given
#   test outcome

prop.table(x=tab, margin="test")

