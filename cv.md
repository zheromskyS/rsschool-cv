# Junior Developer Resume

## Stanislav Zheromsky

### Contact Information

- _Email:_ stanislawzheromsky@gmail.com
- _Mobile phone number (Viber, Telegram):_ 8-033-682-98-38
- _GitHub:_ zheromskyS

### Personal Information

I’m hardworking, patient and stress-resistant person, who interested in programming because this occupation provides endless possibilities for professional growth.
I want to become a front-end developer. Desire to develop and improve my skills helps me to reach my goal. Сreativity, ability to work in a team, logical thinking are important for working as a developer and present in me.

### Skills

- HTML5, CSS3
- C++, Python, JavaScript
- Git, Github
- VS Code, WebStorm, Figma

### Code examples

There is a program finding the shortest path between 2 objects (C++):

```
const int INF = 1e9 + 7;

vector<pair<int, int>> graph[100000];
int ans[100000];
int pr[100000];

int main() {
    int n, m, start, end;
    cin >> n >> m >> start >> end;
    vector<pair<int, int>> g(n);
    for (int i = 0, u, v, c; i < n; i++) {
        cin >> u >> v >> c;
        g[u].push_back({v, c});
        g[v].push_back({u, c});
    }

    for (int i = 0; i < n; i++) {
         ans[i] = INF;
         pr[i] = -1;
    }

    ans[start] = 0;

    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> q;

    q.push({0, start});

    while (!q.empty()) {
       pair<int, int> c = q.top();
       q.pop();

       int dst = c.first, v = c.second;
            if (ans[v] < dst) {
                continue;
            }

       for (pair<int, int> e: graph[v]) {
            int u = e.first, len_vu = e.second;

            int n_dst = dst + len_vu;
            if (n_dst < ans[u]) {
                ans[u] = n_dst;
                pr[u] = v;
                q.push({n_dst, u});
            }
       }
    }

    vector<int> path;

    int cur = end;
    path.push_back(cur);

    while (pr[cur] != -1) {
        cur = pr[cur];
        path.push_back(cur);
    }

    reverse(path.begin(), path.end());

    cout << "Shortest path between vertices " << start + 1 << " and " << end + 1 << " is: " << endl;

    for (int v: path) {
        cout << v + 1 << ", ";
    }
}
```

There is a code-example оf a horizontal site menu (HTML):

```
<header class="header">
    <div class="tool-bar">
         <div class="tool-bar__left-group">
            <div class="language-switcher tool-bar__language-switcher">
                <a class="language-switcher__link" href="#">
                    <img class="language-switcher__size" src="/index/pictures_in_index/language-switch-button.png"
                        alt="кнопка переключения языков">
                </a>
            </div>

            <div class="logo tool-bar__logo">
                <a class="logo__link" href="index.html">
                    <img class="logo__size" src="index/pictures_in_index/HTML5.png" alt="logo">
                </a>
            </div>
        </div>

        <div class="tool-bar__central-group">
            <nav class="tool-bar__sections">
                <ul class="sections-list tool-bar__sections-list">
                    <li class="sections-list__item tool-bar__item">
                        <a href="index.html" class="section-list__link tool-bar__link">Учебник</a>
                    </li>

                    <li class="sections-list__item tool-bar__item">
                        <a href="#" class="section-list__link tool-bar__link">Тесты знаний</a>
                    </li>

                    <li class="sections-list__item tool-bar__item">
                        <a href="#" class="section-list__link tool-bar__link">О проекте</a>
                    </li>
                </ul>
            </nav>
        </div>

<div class="theme-color-switcher tool-bar__theme-color-switcher tool-bar__right-group">
            <a class="theme-color-switcher__link" href="#">
                <img class="theme-color-switcher__size"
                    src="index/pictures_in_index/theme-color-switcher-to-black.png"
                    alt="кнопка переключения языков">
            </a>
        </div>
    </div>
</header
```

### Experience

- Project 'Html and css tutorial for high school' _(HTML, CSS)_
- Project 'Html and css tutorial for high school' _(HTML, CSS)_
- Scientific work 'Decentralized exchange platform' _(React)_
- Rsscool tutorial 'Friday live codding' _(HTML, CSS, JavaScript)_

### Education

- HTML and CSS Tutorials on the Code-basic (completed)
- HTML and CSS Tutorials on the HTML Academy (completed)
- RS Schools Course «JavaScript/Front-end. Stage 0» (completed)
- General secondary education in Gymnasium (in progress)
- Version Control with Git on learn.epam (completed)

### English

- A2 _level_