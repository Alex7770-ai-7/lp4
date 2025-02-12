import random


class CipherObject:

    def init(self, a, b):
        self.__a = a  
        self.__b = b
        self.__operation = random.choice(["+", "-", "*", "/"]) 
        self.result = self.calculate() 

    def __calculate(self):
        if self.__operation == "+":
            return self.a + self.b
        elif self.__operation == "-":
            return self.a - self.b
        elif self.__operation == "*":
            return self.a * self.b
        elif self.__operation == "/":
            return self.a / self.b if self.__b != 0 else "Ділення на 0"

    def str(self):
        """Вивід об'єкта показує результат операції."""
        return f"Результат: {self.result} (Операція: {self.operation})"



cipher = CipherObject(10, 5)
print(cipher)
