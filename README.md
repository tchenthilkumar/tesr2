def asteroidMonitor (year, pha): 
    url= "https://jsonmock.hackerrank.com/api/asteroids/search" 
    page = 1 
    asteroids = []
    while True:
        response requests.get(url, params={"page":page}) 
        data = response.json()
        for asteroid in data['data']: 
            discovery_year = int(asteroid['discovery_date'].split('-')[0])
            if discovery_ year = year and (asteroid['pha'] == pha) 
            period_yr float(asteroid['period_yr']) if asteroid['period_yr'] else 0
            
            asteroids.append ((asteroid['designation'],period_yr))
            if page >= data['total_pages']:
                break
            page += 1
    asteroids.sort(key=lambda x: x[1]) 
    # asteroid[0] for asteroid in asteroids
    val2 = [asteroid[0] for asteroid in asteroids] #print(type(asteroids)) # [asteroid[0] for asteroid in asteroids] first_element = val2[0]
    return first_element
main
