                                                                            # LIZZETH MARCELA LASSO E.
                                                                              Ingeniera de sistemas
                                                                                 Systems Engineer

from __future__ import annotations

import json
from dataclasses import asdict, dataclass


@dataclass
class Arsenal:
    languages: tuple[str, ...] = ("Java","C#", ".NET","Python", "PHP" "JS", "Go")
    databases: tuple[str, ...] = ("SQLite", "PostgreSQL", "MongoDB", "SqlServer")
    misc     : tuple[str, ...] = ("Nodejs", "Selenium", "Laravel", "Express", "OutSystems")
    ongoing  : tuple[str, ...] = ("RPA", "DataScience")

    def jsonify(self) -> str:
        return json.dumps(asdict(self), indent=4)


arsenal = Arsenal()
print(arsenal.jsonify())




