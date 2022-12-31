# Making Work Visible: Exposing Time Theft To Optimize Work & Flow

ในขณะที่จำนวนนาทีที่เรามีอยู่ในแต่ละวันอาจจะเท่ากัน แต่การควบคุมสิ่งที่เราทำในเวลานั้น ๆ แตกต่างกันอย่างมาก

Wasted time can never be regained.

จำนวน requests กับจำนวนเวลาที่คนเราทำได้มันมักจะไม่เท่ากันเลย ดังนั้นเราจำเป็นต้องใช้ “pull system” ซึ่งเราสามาถที่จะ focus ในสิ่งที่เราทำอยู่ใน one thing at the time ก่อนที่เราจะไปเริ่มทำสิ่งใหม่

> The aim of kanban is to make troubles come to the surface.
> 

— Taiichi Ohno

## Part 1: The Five Thieves of Time

### Too Much WIP

วัดเรื่องค่า WIP โดยใช้ cycle time ซึ่งจะสามารถเห็นได้ว่าถ้า WIP ยิ่งสูง cycle time ก็จะยิ่งสูงตามไปด้วย → เกิด cost of delay

WIP เป็น leading indicator ของ cycle time

Context switching เป็นผลกรรมที่มาจากการที่เรามี WIP เยอะเกินไป 

### Unknown Dependencies

เวลาเราพูดถึง dependencies ก็จะมีประมาณอยู่ 3 แบบ

1. Architecture — ที่เวลาแก้ของหนึ่งอย่าง ไปกระทบกับอีกอย่าง
2. Expertise — เรื่อง specific know-how
3. Activity — เรื่องที่เราจะทำของอย่างหนึ่ง แล้วต่อรออีกอย่างหนึ่งให้เสร็จก่อน

> Every dependency doubles your change of being delayed or late.
> 

— Troy Magennis

เวลาเรามี dependencies มากขึ้น โอกาสที่จะทำให้เกิด delay ก็สูงขึ้นด้วย เช่นถ้ามี 2 inputs เราจะมี 4 combinations คือ 00, 01, 10, 11 ซึ่ง 00 หมายถึงเราจะส่งมอบงานได้ on time ส่วนที่มี 1 คือ เกิดปัญหาเรื่อง dependency เลยจะทำให้ส่งมอบช้า

ยิ่งถ้าเรามี 3 inputs แล้ว มันก็จะเกิด 8 combinations โอกาสที่จะส่งมอบงานได้ on time คือ 1/8

### Unplanned Work

Unplanned work == Interruption และงานพวกนี้จะขโมยเวลาของเราไป

งาน urgent ต่าง ๆ จะทำให้เราต้องโดนขัดจังหวะอยู่เสมอ เช่น incident บน production

Unplanned work บางทีเราก็ต้องยอมรับมัน แต่ถ้าเราจะทำให้เราสามารถจัดการสิ่งต่าง ๆ เหล่านี้ได้ดีขึ้น คือทำให้ work ของเรา visible บนบอร์ด เราจะได้ตัดสินใจได้ดีขึ้นว่าควรจะทำเลยหรือว่าเอาไว้ก่อน

การวางแผนสำหรับ unplanned work สามาถทำได้โดยการ reserve capacity ไว้ล่วงหน้า

### Conflicting Priorities

มี one most important thing ซึ่งต้องทำให้ทุกคนรู้ว่ามันคืออะไร

### Neglected Work

Neglected work จะคอยปลูก technical debt ไปเรื่อย ๆ เพราะเรามักจะสนใจสิ่งที่สร้าง value มากกว่าสิ่งที่จะคอยป้องกันปัญหาที่จะเกิดขึ้นในอนาคต

ลองดูว่าโปรเจคไหนเป็น zombie project บ้าง ประเมิน impact ของโปรเจคนั้น ดูว่าจะเก็บไว้ต่อหรือจะลบทิ้งไป

## Part 2: How to Expose Time Thief to Optimize Workflow

สิ่งต่าง ๆ ถ้าเราทำให้เป็นภาพ เราจะสามารถมองปัญหาได้ชัดขึ้น แก้ได้ง่ายขึ้น และตัดสินใจได้ง่ายขึ้นด้วย การทำ making work visible เป็นการทำให้งานของเราดีขึ้น

### Make Work Visible

เราอาจจะมี guideline ในการสร้างการ์ด เช่น ถ้ามีข้อใดข้อหนึ่งในนี้

1. ถ้ามีคนเดียวที่รู้ว่าจะต้องทำอย่างไร
2. งาน impact ทีมอื่น
3. งานปกติที่มีคนทำร่วมด้วยอยู่ ที่เป็น invisble การสร้างการ์ดพวกนี้ออกมา จะทำให้เราเห็น ละไม่ก่อให้เกิด WIP ที่มากเกินไป

Systems Thinking สามารถนำเอามาใช้ได้ เพื่อ optimize workflow across all teams

คนทำงานทุกคนต้องมีส่วนร่วมในการออกแบบ workflow เสมอ

Visuals can show business pain points and other hidden information.

### Ambush the Ringleader

ใช้ WIP limit เป็นตัวกำหนด ที่ team level เพื่อที่จะได้ optimize workflow ในภาพรวม

เราสามารถใช้ horizontal swimlane และกำหนด WIP limit แต่ละ swimlane ได้

เราสามารถกำหนด WIP limits ตาม work type ได้ด้วยเช่นกัน เช่น WIP limit สำหรับงานที่มาจากเบื้องบน

### Expose Dependencies

มีหลายวิธีที่เราจะ expose dependencies ได้ เช่นทำ dependency matrix หรือติด dependency tag หรือทำ dependencies ในงานระหว่างทีม

ตรงนี้จะช่วยให้เราสามารถมองเห็นได้ว่าจะมีงานอะไรเข้ามาบ้าง และเห็นว่าจะมี issue อะไรที่เราจะต้องรับมือก่อน

ถึงแม้ทีมจะเล็กแค่ไหน จะไปไวแค่ไหนก็ตาม แต่ถ้ามี dependencies เข้ามาเมื่อไหร่จะทำให้เราไปช้าทันที

การออกแบบบอร์ด เราต้องทำให้ dependencies ต่าง ๆ ชัดเจนด้วย

### The Perfect Crime-Unplanned Work

เราสามารถทำให้ interruption แสดงตัวออกมาให้เห็นได้ โดยการใช้ dot บนการ์ดที่เราโดน interrupt ถ้ามี 4 dots → โดน interrupt ไป 4 ครั้ง

การที่เราได้รู้ ratio ของ unplanned work กับ planned work จะช่วยให้เราเห็น workload capacity ได้ และจะทำให้เรามี idea ในการตั้ง WIP limits มากขึ้น

การทำ office hours หรือพวก do not disturb hours จะช่วยลดผลกระทบจาก unplanned work ได้

### Prioritize, Prioritize, Prioritize

หา prioritization policy สำหรับทีม

สร้าง line of commitment ซึ่งอะไรที่ข้ามเสร็จนี้แล้ว เรา commit ว่าจะ move forward ไปทำให้เสร็จ

### Prevent Negligence

> Never let something important become urgent
> 

— Eliyahu Goldratt

วิธีที่เราจะทำให้ neglected work เห็นได้ เราอาจจะใส่ againg เข้าไปในการ์ด → Visualize delays

### Useful Board Design Examples

เป็นตัวอย่างบอร์ดต่าง ๆ สามารถมาดูเอาแนวคิดได้

## Part 3: Metrics, Feedback, and Circumstances

### Your Metrics or Your Money

Use metrics → lead time, cycle time to help make good decisions on priorities

Use WIP limits

อย่าให้ทีมทำ 100% capacity เพราะตรงนี้จะทำให้งาน delay (จาก queuing theory)

### The Time Thief O’Gram

นับจำนวน work item type ที่อยู่ในบอร์ด เราจะได้เห็นว่าตอนนี้มีงานประเภทไหนอยู่เท่าไหร่ แล้วก็ track แบบนี้ไป over time จะได้เห็นว่าเราควรจะปรับปรุงให้ดีขึ้นอย่างไร

### Operations Review

เราจะนำเอา metrics ต่าง ๆ มานั่ง review กัน ดูว่าจะปรับปรุงอย่างไรได้บ้าง ทำเป็น recurring review เลย ส่วน metrics ที่จะดูก็มี

- Throughput คือเราทำงานอะไรเสร็จไปแล้วบ้าง มีจำนวน incoming requests เท่าไหร่ และมีที่ทำเสร็จไปแล้วเท่าไหร่ แล้วก็ WIP Limit ในแต่ละ stage
- Flow time
- Issues และ blocked work items ต่าง ๆ มีอะไรบ้าง
- The Time Thief O’Gram

แล้วก็ metrics อื่น ๆ เช่น

- Aging reports
- Card type distribution
- Failure load
- Flow efficiency

### The Art of the Meeting

ใช้ Lean Coffee

### Beastly Practices

- เอาวันหยุดออกจาก flow time → ตัดคำถามต่าง ๆ ทิ้งไป ว่าวันหยุดแบบไหนนับ หรือไม่นับ → นับให้หมดไปเลย → สื่อสารง่ายกว่า
- ลงเวลาใน timesheets เพื่อ track → บางงานไม่ส่งผลต่อ business value แล้วลูกค้าก็ไม่สนใจว่าเราจะทำอะไรเพื่อให้งานเสร็จด้วย
- ใช้ Gantt charts (can’t charts) → แทนที่จะใช้มัน เราจัดการงานใน queue ดีกว่า แล้วให้ดูจำนวนงาน และ wait time แทน
- สร้าง swimlanes เป็นชื่อคน → ความเป็นทีมจะหายไป คนก็จะรู้สึกแบ่งงานกัน ไปแตะงานของคนอื่นไม่ได้ สุดท้ายแล้วก็จะไม่ช่วยกัน deliver งาน → ถ้าเรื่องนี้เกิดขึ้น ให้ค่อย ๆ ปรับ อาจจะรวม lane ที่มี skillset เดียวกันก่อนเป็น step แรก
- Work scattered everywhere → มีประชุมเยอะเกินไป หรือว่ามีอะไรให้ติดตามงานหลายอย่าง ใช้ tools เยอะเกินไป
- Garnish Card Colors → ทำสีให้น่าดึงดูดการใช้งาน และ engaged อย่าทำให้สับสน และเสียเวลา
- Best Practices → “No best practices” → Experiment and learn