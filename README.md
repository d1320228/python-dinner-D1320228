# ==========================================
# Python 聚餐費用試算機 - 完整程式碼
# 學號：D1320228 姓名：蘇子瑜
# ==========================================

print("=== 第一組測試 (原始資料) ===")
event_name = " WEEKEND DINNER "
meal_amount = " NT$1,200 "
people = "4"
service_rate = 0.10
discount = 100
budget_per_person = 300

# 1. 整理聚餐名稱：去除頭尾空白並轉小寫
clean_event_name = event_name.strip().lower()

# 2. 整理餐費與人數並轉換型別
clean_meal_text = meal_amount.replace("NT$", "").replace(",", "").strip()
original_meal = float(clean_meal_text)
num_people = int(people)

# 3. 分步計算費用
service_fee = original_meal * service_rate
total_amount = original_meal + service_fee - discount
cost_per_person = total_amount / num_people

# 4. 判斷是否超過預算 (回傳布林值)
is_over_budget = cost_per_person > budget_per_person

# 5. 輸出費用摘要
print(f"聚餐名稱：{clean_event_name}")
print(f"原始餐費：{original_meal:.2f} 元")
print(f"服務費：{service_fee:.2f} 元")
print(f"折價券：{discount:.2f} 元")
print(f"應付總額：{total_amount:.2f} 元")
print(f"分攤人數：{num_people} 人")
print(f"每人費用：{cost_per_person:.2f} 元")
print(f"每人預算：{budget_per_person:.2f} 元")
print(f"是否超過預算：{is_over_budget}\n")


print("=== 第二組測試 (修改分攤人數為 5 人) ===")
people = "5"  # 修改人數

clean_event_name = event_name.strip().lower()
original_meal = float(meal_amount.replace("NT$", "").replace(",", "").strip())
num_people = int(people)

service_fee = original_meal * service_rate
total_amount = original_meal + service_fee - discount
cost_per_person = total_amount / num_people
is_over_budget = cost_per_person > budget_per_person

print(f"聚餐名稱：{clean_event_name}")
print(f"原始餐費：{original_meal:.2f} 元")
print(f"服務費：{service_fee:.2f} 元")
print(f"折價券：{discount:.2f} 元")
print(f"應付總額：{total_amount:.2f} 元")
print(f"分攤人數：{num_people} 人")
print(f"每人費用：{cost_per_person:.2f} 元")
print(f"每人預算：{budget_per_person:.2f} 元")
print(f"是否超過預算：{is_over_budget}\n")


print("=== 第三組測試 (人數恢復 4 人，折價券改為 220 元) ===")
people = "4"      # 人數恢復
discount = 220    # 修改折價券

clean_event_name = event_name.strip().lower()
original_meal = float(meal_amount.replace("NT$", "").replace(",", "").strip())
num_people = int(people)

service_fee = original_meal * service_rate
total_amount = original_meal + service_fee - discount
cost_per_person = total_amount / num_people
is_over_budget = cost_per_person > budget_per_person

print(f"聚餐名稱：{clean_event_name}")
print(f"原始餐費：{original_meal:.2f} 元")
print(f"服務費：{service_fee:.2f} 元")
print(f"折價券：{discount:.2f} 元")
print(f"應付總額：{total_amount:.2f} 元")
print(f"分攤人數：{num_people} 人")
print(f"每人費用：{cost_per_person:.2f} 元")
print(f"每人預算：{budget_per_person:.2f} 元")
print(f"是否超過預算：{is_over_budget}")
