# Tarea-Prueba-de-Endpoints-y-Guarantee-Event-Consume-Order-en-CQRS-y-Event-Sourcing

## OpenAccountController: Abrir una nueva cuenta.
http://localhost:5000/api/v1/openBankAccount
@PostMapping
{
  "accountHolder": "big boy",
  "accountType": "SAVINGS", // o "CURRENT"
  "amount": 100000.00 // O cualquier balance inicial
}
![image](https://github.com/user-attachments/assets/5a169382-909e-42ce-b965-296876bea551)
"id": "43ffb168-bcf9-4a20-9d2a-b9f5889f8f37"
## DepositFundsController: Depositar fondos.
http://localhost:5000/api/v1/depositFunds/2c25f6d6-6458-469d-8177-cf28a280e5e8
@PutMapping
{
  "amount": 100000.00 // O cualquier balance inicial
}
![image](https://github.com/user-attachments/assets/78d71bdc-1bbc-44b3-8e99-78d888e0917f)
## WithdrawFundsController: Retirar fondos.
http://localhost:5000/api/v1/withdrawFunds/2c25f6d6-6458-469d-8177-cf28a280e5e8
PutMapping
{
  "amount": 10.00 // O cualquier balance inicial
}
![image](https://github.com/user-attachments/assets/90815f6b-e1bc-4118-b646-93c6e593e6a3)
## CloseAccountController: Cerrar la cuenta.
http://localhost:5000/api/v1/closeBankAccount/2c25f6d6-6458-469d-8177-cf28a280e5e8
@DeleteMapping
![image](https://github.com/user-attachments/assets/8d85ba78-783a-4e7c-bbc4-15c78c95072e)
## AccountLookupController: Consultar cuentas.
### a.
@GetMapping
http://localhost:5001/api/v1/bankAccountLookup/
![image](https://github.com/user-attachments/assets/334e8e73-ac5e-4512-b762-3443b14c0261)
![image](https://github.com/user-attachments/assets/02986398-3d12-4d1f-af83-72088e302267)
### b.
@GetMapping
http://localhost:5001/api/v1/bankAccountLookup/byId/0694a202-13e3-4fe8-b31d-576d2956dc11
![image](https://github.com/user-attachments/assets/dc4b93f9-ee97-40fc-9108-e12479b15a06)
![image](https://github.com/user-attachments/assets/5262a7d7-8595-40a6-978d-4a5a3654c665)
### c.
@GetMapping
http://localhost:5001/api/v1/bankAccountLookup/byHolder/BIC MICHUM
![image](https://github.com/user-attachments/assets/257e8aff-0b93-4e70-a7b2-d190b719a021)
![image](https://github.com/user-attachments/assets/33818fc4-ec80-47e7-a392-a32dbb1649f4)
### d.
@GetMapping
http://localhost:5001/api/v1/bankAccountLookup/withBalance/GREATER_THAN/200
![image](https://github.com/user-attachments/assets/b710f5a7-2f17-483e-b4cd-a732de415005)
![image](https://github.com/user-attachments/assets/e00ff341-b1ea-41fc-8ef9-0799c916c127)

## RestoreReadDbController: Restaurar la base de datos de lectura.
@PostMapping
http://localhost:5000/api/v1/restoreReadDb
![image](https://github.com/user-attachments/assets/0ef7c51d-0d53-44b5-80f3-efc27c65f979)

___________________________________________________________________________________________________________
# PARTE 2: : Guarantee Event Consume Orde







