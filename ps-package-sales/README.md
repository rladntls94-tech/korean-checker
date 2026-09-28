# PS 패키지 판매량 정리

SIE **SKU Sales Cube** CSV(`C04_ SKU Sales Cube_ Last 3 months by day and SKU_Finance Team.csv`)를 넣으면
상품별 Sales Quantity를 날짜별로 합산해 `통합` 시트에 바로 붙여넣을 수 있는 형태로 정리합니다.

- `index.html`을 브라우저로 열면 됩니다. 설치 필요 없음, 오프라인 동작.
- CSV는 브라우저 안에서만 처리되며 어디에도 업로드되지 않습니다. 이 저장소에는 판매 데이터가 포함되어 있지 않습니다.

## 정리 항목 (통합 시트 B~G)
| 열 | 항목 | CSV Product Name |
|---|---|---|
| B | 사전 다운로드/무료 업그레이드 | Black Desert – PlayStation 5 Upgrade Install ... |
| C | Edition · Standard | Black Desert : Standard Edition |
| D | Edition · Heroic | Black Desert: Heroic Edition |
| E | Edition · Mythical | Black Desert : Mythical Edition |
| F | Item · Heroic | Black Desert: Heroic Item Pack |
| G | Item · Mythical | Black Desert: Mythical Item Pack |

## Temporal
한 줄에 한 열씩 `라벨 = 키워드` 형식으로 입력합니다. 키워드와 정확히 같은 상품명이 있으면 그 상품만,
없으면 이름·Product ID에 키워드가 포함된 상품을 모두 합산합니다.

집계 기준: 환불·무료·바우처를 포함한 전체 Sales Quantity 합계 (엑셀 SUMIFS와 동일).
