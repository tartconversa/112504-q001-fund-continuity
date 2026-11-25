# 双基金运营经费的存续测算与接续承诺

资金记录的金额统一为元，月份以公历月统计。费用类别存在待裁定项。到账日期空白表示在接收资料时尚无记录。较早验收是同一拨款方的历史协议，资金清单列当前新周期额度。已续签岗位的生效和签署时点分别记载。

## 资料

CSV 样例为合成记录，使用 UTF-8，首行为字段名。多值用竖线分隔，空单元格表示来源未填。记录日期和业务生效日期各有含义。

- funds.csv 的字段为 fund、payer、use、limit、active_from、active_to、condition。
- accepted.csv 的字段为 claim、fund、project、amount、due、accepted_at、paid_at、recorded_at、rev。
- staff_hours.csv 的字段为 interval、person、project、month、hours、allocation、class、rev。
- commitments.csv 的字段为 contract、party、project、start、end、fee_month、state、signed_on。
- scenarios.csv 的字段为 id、payer、delay_days、topup、topup_month。
- policy.csv 的字段为 year、management_ceiling、as_of、initial_free_cash。

## 运行资料检查

在项目根目录使用 Python 3.11 或更高版本。依赖仅为标准库。

~~~sh
python3 -m compileall -q tests
python3 -m unittest discover -s tests -v
~~~
