from bs4 import BeautifulSoup
import csv

html_code = """
...  # Paste your HTML code here
"""

soup = BeautifulSoup(html_code, 'html.parser')

%% # Extract title, list, and links %%
sections = []

for title_tag in soup.find_all('strong'):
    section = {'title': title_tag.get_text(strip=True), 'list': [], 'links': []}
    
    # Extract list items and associated links
    list_tag = title_tag.find_next('ul')
    if list_tag:
        for item in list_tag.find_all('li'):
            link_tags = item.find_all('a')
            links = [link['href'] for link in link_tags] if link_tags else []
            
            section['list'].append(item.get_text(strip=True))
            section['links'].append(links)
    
    sections.append(section)

%% # Write data to CSV file %%
csv_file_path = 'output.csv'

with open(csv_file_path, 'w', newline='', encoding='utf-8') as csv_file:
    csv_writer = csv.writer(csv_file)
    
    # Write header
    csv_writer.writerow(['Title', 'List', 'Links'])
    
    # Write data
    for section in sections:
        csv_writer.writerow([section['title'], ', '.join(section['list']), ', '.join(map(str, section['links']))])

print(f"CSV file has been created: {csv_file_path}")



how to run got to the cmd then cd the pile path 
then run python3 name_of_the_file.py
in my case my file in my home 

run this command python3 name_of_the_file.py
name of the file is extract.py 
extract2.py








error

"or check the file name if there is a symbol that not require in saving the csv file"

Traceback (most recent call last):
  File "/home/ken/extract.py", line 13533, in <module>
    links = [link['href'] for link in link_tags] if link_tags else []
  File "/home/ken/extract.py", line 13533, in <listcomp>
    links = [link['href'] for link in link_tags] if link_tags else []
  File "/home/ken/.local/lib/python3.10/site-packages/bs4/element.py", line 1573, in __getitem__
    return self.attrs[key]
KeyError: 'href'



from bs4 import BeautifulSoup
import csv

html_code = """
...  # Paste your HTML code here
"""

soup = BeautifulSoup(html_code, 'html.parser')

# Extract title, list, and links
sections = []

for title_tag in soup.find_all('strong'):
    section = {'title': title_tag.get_text(strip=True), 'list': [], 'links': []}
    
    # Extract list items and associated links
    list_tag = title_tag.find_next('ul')
    if list_tag:
        for item in list_tag.find_all('li'):
            link_tags = item.find_all('a')
            
            # Check if 'href' attribute exists before accessing it
            links = [link.get('href', '') for link in link_tags]
            
            section['list'].append(item.get_text(strip=True))
            section['links'].append(links)
    
    sections.append(section)

# Write data to CSV file
csv_file_path = 'output.csv'

with open(csv_file_path, 'w', newline='', encoding='utf-8') as csv_file:
    csv_writer = csv.writer(csv_file)
    
    # Write header
    csv_writer.writerow(['Title', 'List', 'Links'])
    
    # Write data
    for section in sections:
        csv_writer.writerow([section['title'], ', '.join(section['list']), ', '.join(map(str, section['links']))])

print(f"CSV file has been created: {csv_file_path}")






