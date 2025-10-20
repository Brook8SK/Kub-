url = 'https://api.hh.ru/vacancies'
params = {
    'text': 'Python',    
    'area': 113,          
    'per_page': 10         
}

response = requests.get(url, params=params)
data = response.json()

for vacancy in data['items']:
    print(vacancy['name'])          
    print(vacancy['employer']['name']) 
    print(vacancy['alternate_url'])   
    print('-' * 30)
