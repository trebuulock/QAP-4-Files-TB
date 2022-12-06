# The One Stop Insurance Company
# Author: Tre Bullock

# Constants
PolicyNum = 1944
BasicPrem = 869.00
DiscAdd = .25
LiabilityCov = 130.00
GlassCovCost = 86.00
LoanCov = 58.00
HST_RATE = .15
ProcessFee = 39.99

# Inputs
CusFirstName = input("Please Enter Your First Name ")
CusLastName: str = input("Please Enter Your Last Name ")
StreetAddress = input("Please Enter Your Current Street Address ")
CusCity = input("Please Enter Your Current Residing City ")
CusProvince = input("Please Enter Your Current Residing Province ")
CusPostCode = input("Please Enter Your Current Postal Code ")
CusNumber = input("Please Enter Your Current Cellphone Number ")
NumCars = input("Please Enter The Number Of Vehicles Included On The Plan ")
ExtraLiability = input("Include Extra Liability Up To $1000000? (Y/N)  ")
GlassCov = input("Include Extra Glass Coverage? (Y/N) ")
LoanCar = input("Include Loan Car? (Y/N) ")
PayPlan = input("Would You Like To Pay In Full Or Monthly? (F/M) ")
TotalExtraCost = (ExtraLiability + GlassCov + LoanCar)
TotalCost = (input((TotalExtraCost + BasicPrem + ProcessFee) * 1.15))
MonthCost = input(TotalCost / 8)

# Processes
if ExtraLiability == "Y":
    print(LiabilityCov)
else:
    print(0)

if GlassCov == "Y":
    print(GlassCovCost)
else:
    print(0)

if LoanCar == "Y":
    print(LoanCov)
else:
    print(0)
    
if PayPlan == "F":
    print(TotalCost) 
else: 
    print(MonthCost)


# Outputs 
print(CusFirstName)
print(CusLastName)
print(StreetAddress)
print(CusCity)
print(CusProvince)
print(CusPostCode)
print(CusNumber)
print(ExtraLiability)
print(GlassCov)
print(LoanCar)
print(PayPlan)
print(TotalCost)
print("Policy Information Processed And Saved ")
print("Thank You For Choosing One Stop Insurance "

file = open("Policies.dat","a")
f.write("{},".format(str(PolicyNum)))
f.write("{},".format(CusFirstName))
f.write("{},".format(CusLastName))
f.write("{},".format(StreetAddress))
f.write("{},".format(CusCity))
f.write("{},".format(CusProvince))
f.write("{},".format(CusPostCode))
f.write("{},".format(CusNumber))
f.write("{},".format(LiabilityCov))
f.write("{},".format(GlassCov))
f.write("{},".format(LoanCar))
f.write("{},".format(PayPlan))

f.close()

print(" ")
