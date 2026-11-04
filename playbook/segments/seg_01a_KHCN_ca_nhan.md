---
id: SEG-KHCN-CN
used_by: [Propagation, Product-Impact, Inside-out Monitor]
steps: [2, 3, 4]
depends_on: [core/01_risk_codes.md, core/03_linkage_graph.md]
load_when: Sự kiện chạm cá nhân/hộ gia đình, hoặc lan tới KHCN qua L01, L02, L04, L05, L06
version: v3.0
updated: 2026-11-02
---

# Phân khúc KHCN – nhóm cá nhân

> KHCN gồm hai nhóm: **cá nhân** (file này) và **hộ kinh doanh** (`segments/seg_01b_KHCN_ho_kinh_doanh.md`). Khi sự kiện chạm chủ hộ kinh doanh, nạp cả hai file.

> Cấu trúc: (a) Chân dung → (b) Động lực rủi ro → (c) Bảng độ nhạy sản phẩm → (d) Tín hiệu sớm nội bộ → (e) Lan ra phân khúc khác → (f) Danh mục sản phẩm & URL nguồn


## (a) Chân dung & phân hạng
| Phân hạng | Đặc điểm | Ý nghĩa cho suy luận |
|---|---|---|
| Đại chúng | Người làm công ăn lương, thu nhập chủ yếu qua TK thanh toán | Nhạy với việc làm, lương, lạm phát, lừa đảo |
| Inspire | Khách hàng trẻ, số hóa cao, dùng thẻ/app nhiều | Nhạy với sự cố app, lừa đảo số, tín dụng tiêu dùng |
| Priority | Khách hàng giàu có, nhiều sản phẩm đầu tư/bảo hiểm | Nhạy với thị trường vốn, BĐS; **thường là chủ DN/HKD (cạnh L01)** |
| Private / Techcom Wealth | Khách hàng siêu giàu, quản lý gia sản | Tập trung rủi ro lớn, liên kết chặt với DN sở hữu, nhạy với tin pháp lý cá nhân |

## (b) Động lực rủi ro chính
1. **Thu nhập & việc làm** (sa thải, giảm lương, ngành gặp khó)
2. **Lãi suất** (khoản vay thả nổi mua nhà/ô tô; hấp dẫn của tiết kiệm vs đầu tư)
3. **Giá tài sản** (BĐS, chứng khoán, trái phiếu, vàng)
4. **Sức khỏe & thiên tai** (bệnh tật, dịch bệnh, bão lũ)
5. **Lừa đảo & an ninh số** (mạo danh, chiếm đoạt tài khoản)
6. **Pháp lý cá nhân** (khởi tố, phong tỏa tài sản, tranh chấp)
7. **Quy định** (xác thực sinh trắc, hạn mức giao dịch, thuế thu nhập)

## (c) Bảng độ nhạy sản phẩm KHCN

**Nhóm Chi tiêu – Tài khoản, Thẻ, Dịch vụ**

| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CN-ACC-01` | Tài khoản thanh toán | `LQ` `FR` `OR` `CO` | **P1:** mạo danh ngân hàng, tin nhắn/cuộc gọi giả danh, web giả; mua bán, thuê tài khoản; sự cố app, gián đoạn chuyển tiền, lỗ hổng CVE Android/iOS; tin đồn thanh khoản, rút tiền hàng loạt<br>**P2:** cắt giảm lao động, chậm lương, giãn việc; sinh trắc học, quy định mở tài khoản (QĐ 2345)<br>**P3 (+):** tuyển dụng lớn, nhà máy/KCN mới, tăng lương tối thiểu | **P1:** tiền khách bị chuyển đi; tài khoản bị dùng làm trung gian; CASA rút nhanh sang ngân hàng khác; tăng khóa TK, tra soát, khiếu nại<br>**P2:** số dư lương về giảm; tài khoản chưa xác thực bị hạn chế giao dịch<br>**(+):** tài khoản lương mới, CASA tăng |
| `CN-ACC-02` | Tài khoản ngoại tệ | `MR` `CO` | **P2:** quy định ngoại hối, hạn mức ngoại tệ cá nhân; USD/VND tăng mạnh, VND mất giá, Fed tăng lãi suất<br>**P3:** kiều hối giảm, siết visa lao động<br>**P3 (+):** kiều hối mùa cuối năm, du lịch nước ngoài, mùa du học | **P2:** số dư VND chuyển sang ngoại tệ, áp lực trạng thái ngoại tệ của ngân hàng; giao dịch cần rà soát<br>**P3:** tiền về quốc tế giảm theo tỉnh<br>**(+):** số dư ngoại tệ và giao dịch chuyển đổi tăng |
| `CN-ACC-03` | Sinh lời tự động | `LQ` `MR` `RP` | **P1:** sự cố sản phẩm sinh lời (chậm rút, lỗi tính lãi)<br>**P2:** ngân hàng khác tăng lãi suất huy động, cuộc đua lãi suất; chứng khoán tăng nóng, vàng lập đỉnh, sốt đất<br>**P3:** lãi suất điều hành, liên ngân hàng giảm; quy định bảo vệ người tiêu dùng tài chính<br>**P2 (+):** tin đồn ở ngân hàng khác | **P1:** mất niềm tin, rút đồng loạt, khiếu nại<br>**P2:** tiền chuyển sang nơi lợi suất cao hơn hoặc sang tài sản đang tăng (`G02`)<br>**P3:** lợi suất giảm, kém hấp dẫn; phải điều chỉnh cách giới thiệu sản phẩm<br>**(+):** tiền tìm nơi an toàn chuyển đến (`O6`) |
| `CN-CARD-01` | Thẻ tín dụng | `CR` `FR` | **P1:** lộ dữ liệu thẻ, rò rỉ dữ liệu, cổng thanh toán bị tấn công; gian lận thẻ quốc tế, lừa đảo mua sắm online<br>**P2:** cắt giảm lao động, giảm giờ làm, thu nhập giảm; lạm phát, giá xăng, giá thực phẩm tăng; siết tín dụng tiêu dùng<br>**P3:** ví trả sau, BNPL của đối thủ<br>**P3 (+):** mùa du lịch, lễ Tết, ngày hội mua sắm | **P1:** giao dịch gian lận, tra soát, hoàn tiền tăng; phát hành lại thẻ hàng loạt<br>**P2:** dư nợ quay vòng tăng, chuyển sang trả tối thiểu, DPD tăng<br>**P3:** mất chi tiêu sang đối thủ, khách có nhiều khoản nợ nhỏ ở nơi khác<br>**(+):** chi tiêu thẻ tăng, kèm gian lận mùa cao điểm |
| `CN-CARD-02` | Thẻ thanh toán (ghi nợ quốc tế/nội địa) | `FR` `OR` `BR` | **P1:** sự cố hệ thống thẻ, gián đoạn chuyển mạch, POS lỗi; skimming ATM, lộ dữ liệu thẻ<br>**P2:** chi tiêu giảm, sức mua yếu<br>**P3:** QR, ví điện tử thay thẻ; quy định chuyển đổi thẻ chip<br>**P3 (+):** mùa mua sắm, ưu đãi theo mùa | **P1:** giao dịch thất bại, gian lận theo cụm điểm; tăng tra soát, khiếu nại<br>**P2:** doanh số thẻ giảm<br>**P3:** giao dịch chuyển sang QR; khách chưa đổi thẻ bị gián đoạn<br>**(+):** doanh số thẻ tăng |
| `CN-PAY-01` | Chuyển tiền quốc tế | `CO` `MR` | **P1:** trừng phạt, cấm vận, xung đột ở nước nhận tiền; danh sách FATF, rửa tiền xuyên biên giới, tiền ảo; lừa đảo tình cảm, đầu tư, việc làm ở nước ngoài<br>**P2:** tỷ giá biến động mạnh, USD tăng<br>**P3:** siết visa du học, học phí nước ngoài tăng<br>**P3 (+):** kiều hối, lao động xuất khẩu tăng, mùa du học | **P1:** giao dịch phải dừng, rà soát; khách chuyển tiền cho đối tượng lừa đảo; rủi ro tuân thủ, danh tiếng<br>**P2:** chi phí chuyển đi tăng, khách hoãn giao dịch<br>**P3:** chuyển tiền du học giảm hoặc đổi nước<br>**(+):** giá trị chuyển tiền và phí tăng |
| `CN-PAY-02` | Dịch vụ qua CDM (nộp/rút 24/7) | `OR` `LQ` | **P1:** tin đồn ngân hàng, rút tiền ồ ạt; bão lũ, ngập, mất điện diện rộng; skimming ATM, tiền giả<br>**P2:** giá vàng lập đỉnh, xếp hàng mua vàng; mùa Tết, lễ dài, mùa thu hoạch<br>**P3 (+):** nộp tiền mặt sau vụ mùa | **P1:** rút tiền mặt tăng đột biến (tín hiệu hoảng loạn), máy cạn tiền hoặc dừng hoạt động, mất tiền khách<br>**P2:** rút tiền mặt mua vàng; nhu cầu tiền mặt tăng theo mùa, cần tiếp quỹ<br>**(+):** tiền nộp qua CDM tăng |
| `CN-LOY-01` | OneU (khách hàng thân thiết) | `BR` `FR` | **P2:** chiếm đoạt tài khoản để đổi điểm, mạo danh chương trình ưu đãi<br>**P3:** săn ưu đãi, tạo nhiều tài khoản; đối tác dừng hợp tác, thay đổi thể lệ; quy định khuyến mại, dữ liệu cá nhân<br>**P3 (+):** mùa mua sắm, đối tác mới, hoàn tiền | **P2:** điểm bị đổi trái phép, khiếu nại<br>**P3:** chi phí ưu đãi tăng; giảm tương tác; phải điều chỉnh thu thập dữ liệu<br>**(+):** tương tác và chi tiêu tăng |

**Nhóm Tiết kiệm**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CN-DEP-01` | Tiền gửi tiết kiệm có kỳ hạn | `LQ` `MR` | **P1:** tin đồn ngân hàng, rút tiền hàng loạt<br>**P2:** ngân hàng khác tăng lãi suất huy động; vàng, chứng khoán tăng nóng; thiên tai, dịch bệnh cần tiền mặt<br>**P3:** lãi suất điều hành giảm<br>**P2 (+):** tin đồn ở ngân hàng khác; chốt lời vàng, chứng khoán; tiền về sau thu hoạch | **P1:** tất toán trước hạn hàng loạt, rút tiền mặt (`S07` `F01`)<br>**P2:** không tái tục, chuyển sang nơi lãi cao hoặc tài sản đang tăng (`G02`); rút chi tiêu khẩn cấp<br>**P3:** kỳ hạn ngắn lại (`F02`)<br>**(+):** tiền gửi mới (`O2` `O6`) |
| `CN-DEP-02` | Tích lũy Như Ý | `LQ` | **P2:** cắt giảm lao động, chậm lương, giảm giờ làm; lạm phát<br>**P3:** lãi suất giảm<br>**P3 (+):** tăng lương, thưởng Tết | **P2:** ngừng nộp định kỳ, rút trước hạn<br>**P3:** giảm số tiền nộp<br>**(+):** mở mới, tăng mức nộp |
| `CN-DEP-03` | Tiền gửi rút gốc linh hoạt | `LQ` | **P2:** mất việc, ốm đau, dịch bệnh, thiên tai; giá vàng tăng nóng<br>**P3:** lãi suất đối thủ | **P2:** rút gốc từng phần tăng<br>**P3:** số dư bình quân giảm |
| `CN-DEP-04` | Chứng chỉ tiền gửi Bảo Lộc | `LQ` `MR` `RP` | **P1:** tin đồn về ngân hàng, hạ xếp hạng tín nhiệm<br>**P2:** lãi suất thị trường tăng, kênh đầu tư khác hấp dẫn<br>**P3:** quy định phát hành chứng chỉ tiền gửi<br>**P3 (+):** lãi suất giảm (CCTG lãi cố định hấp dẫn hơn) | **P1:** yêu cầu bán lại tăng, rủi ro danh tiếng<br>**P2:** không mua mới<br>**P3:** phải điều chỉnh sản phẩm<br>**(+):** nhu cầu mua mới |

**Nhóm Vay**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CN-LN-01` | Vay mua nhà dự án trực tiếp từ Chủ đầu tư | `CR` `CL` `RP` | **P1:** dự án bị thanh tra, dừng thi công; chủ đầu tư vỡ nợ trái phiếu, mất thanh khoản<br>**P2:** hết ưu đãi, lãi thả nổi tăng; chậm bàn giao, chậm cấp sổ<br>**P3:** bảng giá đất, luật đất đai, giá BĐS khu vực<br>**P3 (+):** tháo gỡ pháp lý dự án, mở bán lại | **P1:** người mua ngừng trả, tranh chấp với CĐT, TSBĐ hình thành trong tương lai mất giá trị (cạnh `L04`)<br>**P2:** DPD tăng khi hết ân hạn<br>**P3:** LTV xấu đi<br>**(+):** giải ngân mới (`O1`) |
| `CN-LN-02` | Vay mua BĐS có Giấy chứng nhận | `CR` `CL` | **P2:** lãi thả nổi tăng, hết ưu đãi; thu nhập giảm, cắt giảm lao động<br>**P3:** giá BĐS giảm, thanh khoản BĐS thấp, ngập lụt vùng TSBĐ<br>**P3 (+):** lãi suất giảm, sốt đất | **P2:** DPD, xin giãn nợ<br>**P3:** LTV xấu đi, bán gấp TSBĐ (`F03`)<br>**(+):** nhu cầu vay tăng, kèm rủi ro đầu cơ (`G04`) |
| `CN-LN-03` | Vay nhận chuyển nhượng | `CR` `CL` | **P2:** thanh khoản BĐS thứ cấp đóng băng, lãi suất tăng<br>**P3:** thuế chuyển nhượng, quy định giao dịch BĐS<br>**P3 (+):** thị trường thứ cấp sôi động | **P2:** khó bán tài sản để trả nợ, DPD<br>**P3:** giao dịch chậm<br>**(+):** hồ sơ vay tăng |
| `CN-LN-04` | Vay mua ô tô đi lại | `CR` `CL` | **P2:** thu nhập tài xế dịch vụ giảm, giá xăng tăng; hãng giảm giá xe mới<br>**P3:** lệ phí trước bạ, xe điện, hạn chế xe xăng<br>**P3 (+):** giảm lệ phí trước bạ, ưu đãi của hãng | **P2:** DPD; giá xe cũ giảm nhanh hơn dư nợ (`CL`)<br>**P3:** nhu cầu vay dồn rồi giảm sau khi hết ưu đãi<br>**(+):** giải ngân tăng |
| `CN-LN-05` | Tài khoản thấu chi MyCash | `CR` | **P2:** thu nhập giảm, chậm lương, ốm đau, thiên tai; chứng khoán, vàng tăng nóng<br>**P3:** lạm phát | **P2:** sử dụng hạn mức tăng vọt = tín hiệu căng thẳng (`S04`); tiền thấu chi chuyển sang đầu tư (`G01`)<br>**P3:** dư nợ tăng dần |
| `CN-LN-06` | Vay tiêu dùng tín chấp trả góp | `CR` | **P2:** mất việc, sa thải, giảm lương (cạnh `L02`); lạm phát; tín dụng đen, vay qua app<br>**P3:** siết tín dụng tiêu dùng<br>**P3 (+):** tuyển dụng lớn, KCN mới | **P2:** DPD sớm nhất trong danh mục; nợ chồng nợ<br>**P3:** giải ngân giảm<br>**(+):** nhu cầu vay tăng |
| `CN-LN-07` | Vay cầm cố tiền gửi | `CR` (thấp) `LQ` | **P2:** cần tiền gấp: ốm đau, thiên tai, thua lỗ kinh doanh; vàng, chứng khoán tăng nóng | **P2:** khoản vay cầm cố tăng = khách cần tiền nhưng không muốn tất toán (`S06`); hoặc vay để đầu tư (`G02`) |
| `CN-LN-08` | Vay xây dựng / sửa chữa nhà ở | `CR` `CL` | **P2:** giá thép, xi măng, vật liệu tăng; bão lũ, sạt lở<br>**P3:** quy định cấp phép xây dựng<br>**P3 (+):** sửa chữa sau thiên tai, vật liệu giảm giá | **P2:** đội chi phí, công trình dở dang, chậm trả<br>**P3:** chậm giải ngân<br>**(+):** nhu cầu vay sửa chữa |
| `CN-LN-09` | Thấu chi có TSBĐ | `CR` `CL` | **P2:** DN của chủ gặp khó (thuế quan, mất đơn, bị chậm thanh toán); giá BĐS giảm<br>**P3:** lãi suất tăng | **P2:** hạn mức dùng để bơm vốn cho DN (cạnh `L01`, `S12`); TSBĐ giảm giá<br>**P3:** chi phí lãi tăng |
| `CN-LN-10` | Thấu chi không TSBĐ | `CR` | **P2:** thu nhập giảm, chậm lương; chứng khoán tăng nóng | **P2:** hạn mức tăng vọt như MyCash; dùng sai mục đích (`G01`) |

**Nhóm Đầu tư**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CN-INV-01` | Trái phiếu DN iBond (iBond Pro – dòng tiền định sẵn; iBond Prix – đầu tư linh hoạt; iBond Prix – tích lũy bền vững) | `MR` `RP` `LQ` `CO` | **P1:** tổ chức phát hành chậm trả gốc lãi, vỡ nợ, bị điều tra; khủng hoảng trái phiếu<br>**P2:** quy định trái phiếu, nhà đầu tư chuyên nghiệp; lãi suất tăng<br>**P3:** xếp hạng tín nhiệm ngành của tổ chức phát hành<br>**P3 (+):** lãi suất giảm, thị trường trái phiếu phục hồi | **P1:** bán lại đồng loạt, khiếu nại tập thể, rủi ro danh tiếng lớn (cạnh `L05`, `S08`)<br>**P2:** giảm phân phối, điều chỉnh tư vấn<br>**(+):** mua mới tăng, kèm rủi ro mua dồn (`G03`) |
| `CN-INV-02a` | Quỹ trái phiếu Techcom (TCBF) | `MR` `LQ` | **P1:** DN phát hành trong danh mục quỹ vỡ nợ<br>**P2:** lãi suất tăng<br>**P3:** quy định trái phiếu<br>**P3 (+):** lãi suất giảm | **P1:** NAV giảm đột ngột, rút vốn hàng loạt<br>**P2:** NAV giảm, rút vốn<br>**(+):** NAV tăng, dòng tiền vào |
| `CN-INV-02b` | Quỹ cổ phiếu Techcom Top 30 (TCEF) | `MR` | **P2:** chứng khoán giảm mạnh, khối ngoại bán ròng, tỷ giá tăng<br>**P3 (+):** nâng hạng thị trường, chứng khoán tăng | **P2:** NAV giảm; khách Priority tái cơ cấu tài sản<br>**(+):** dòng tiền vào, kèm rủi ro mua đỉnh (`G03`) |
| `CN-INV-02c` | Quỹ cổ phiếu Ngân hàng & Tài chính (TCFIN) | `MR` | **P1:** tin xấu về ngân hàng, kiểm soát đặc biệt<br>**P2:** quy định NHNN, room tín dụng, nợ xấu ngành tăng | **P1:** nhạy kép: NAV giảm và niềm tin vào ngân hàng giảm<br>**P2:** NAV giảm |
| `CN-INV-02d` | Quỹ cổ phiếu DN vừa và nhỏ (TCSME) | `MR` | **P2:** SME khó khăn, thanh khoản thị trường giảm, giải chấp ký quỹ | **P2:** NAV biến động mạnh, rút vốn |
| `CN-INV-02e` | Quỹ cổ phiếu Bất động sản (TCRES) | `MR` | **P1:** chủ đầu tư lớn vỡ nợ, bị điều tra<br>**P2:** chính sách BĐS, siết tín dụng BĐS, lãi suất tăng<br>**P3 (+):** tháo gỡ pháp lý dự án | **P1:** NAV giảm mạnh, rút vốn (cạnh `L04`)<br>**P2:** NAV giảm<br>**(+):** NAV tăng |
| `CN-INV-02f` | Quỹ Cân bằng Linh hoạt (TCFF) | `MR` | **P2:** cổ phiếu và trái phiếu cùng giảm; lãi suất tăng | **P2:** NAV giảm vừa phải, rút vốn |
| `CN-INV-03` | Chứng chỉ tiền gửi (kênh đầu tư) | Xem `CN-DEP-04` | | |

**Nhóm Bảo hiểm**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CN-INS-01` | BH sức khỏe: Song An, Global Prime, An tâm đồng hành, Chăm sóc sức khỏe toàn diện | `INS` `RP` | **P1:** dịch bệnh bùng phát<br>**P2:** ô nhiễm không khí, nắng nóng; chi phí y tế, viện phí tăng<br>**P3:** quy định bancassurance<br>**P2 (+):** dịch bệnh, tin y tế làm nhu cầu tăng | **P1:** claim tăng đột biến<br>**P2:** tranh chấp từ chối bồi thường<br>**P3:** điều chỉnh cách bán<br>**(+):** hợp đồng mới, kèm `RP` nếu bán không đúng nhu cầu |
| `CN-INS-02` | BH tích lũy & đầu tư: Techcom Life Max Chủ Động, Max Vững Vàng, Khỏe trọn vẹn vượt trội, Khỏe bình an vượt trội, Vững tương lai vượt trội | `RP` `LQ` `CO` | **P1:** khủng hoảng niềm tin bảo hiểm, vụ tư vấn sai bị phanh phui<br>**P2:** thu nhập giảm (ngừng đóng phí); quy định bancassurance, cấm bán kèm khoản vay<br>**P3:** lãi suất đầu tư giảm | **P1:** hủy hợp đồng hàng loạt, khiếu nại, rủi ro danh tiếng<br>**P2:** ngừng đóng phí, hủy sớm (`S09`)<br>**P3:** giá trị tài khoản thấp hơn kỳ vọng |
| `CN-INS-03` | BH khác: nhà tư nhân, ô tô, du lịch toàn cầu TechCare Travel | `INS` | **P1:** bão lũ, cháy nổ diện rộng<br>**P2:** tai nạn, gián đoạn đi lại, hủy chuyến bay<br>**P3 (+):** mùa du lịch | **P1:** claim tăng theo địa bàn<br>**P2:** claim du lịch tăng<br>**(+):** bán mới bảo hiểm du lịch |

**Nhóm Ngân hàng số**
| Mã | Sản phẩm | Rủi ro chính | Nhạy với sự kiện | Chiều tác động khi sự kiện xấu |
|---|---|---|---|---|
| `CN-DIG-01` | Techcombank Mobile, Online Banking | `OR` `FR` `RP` | **P1:** sự cố hệ thống, tấn công mạng, lỗ hổng CVE; app giả, mã độc điều khiển từ xa, lừa đảo mạo danh<br>**P2:** quy định xác thực, sinh trắc học<br>**P3:** đối thủ ra tính năng mới | **P1:** gián đoạn mọi sản phẩm khác (mẫu P3); mất tiền khách; bùng nổ khiếu nại mạng xã hội (`S13` `S14` `X07`)<br>**P2:** khách bị hạn chế giao dịch<br>**P3:** giảm tương tác |

## (d) Tín hiệu sớm nội bộ – KHCN
- Lương về tài khoản giảm/không về (theo DN trả lương – cạnh `L02`)
- Tỷ lệ sử dụng hạn mức MyCash / thẻ tín dụng tăng nhanh; chuyển từ trả toàn bộ sang trả tối thiểu
- Tất toán tiết kiệm trước hạn, vay cầm cố tiền gửi tăng
- Rút tiền mặt qua CDM tăng bất thường theo địa bàn
- Bán lại iBond/iFund hàng loạt, nhất là theo một tổ chức phát hành/một ngành
- Hủy hợp đồng bảo hiểm sớm, ngừng đóng phí
- Đổi thiết bị/đăng nhập bất thường, chuyển tiền tới tài khoản mới lần đầu với giá trị lớn (lừa đảo)

## (e) Lan ra phân khúc khác
- **→ HKD/SME bán lẻ** (cạnh `L06`): chi tiêu thẻ/QR giảm = doanh thu HKD giảm (P2).
- **→ DN** (cạnh `L01`): biến cố của chủ DN (pháp lý, sức khỏe, nợ cá nhân) → DN mất người ra quyết định, mất bảo lãnh, mất TSBĐ.
- **→ Cấp ngân hàng** (cạnh `L10`): rút tiền gửi diện rộng, khủng hoảng iBond → thanh khoản, danh tiếng và nhà đầu tư của ngân hàng (`bank/ngan_hang.md`).


## (f) Danh mục sản phẩm & URL nguồn (chốt 26/10/2026)


- **Phân hạng:** Inspire · Priority · Private · Techcom Wealth
- **Chi tiêu – Tài khoản:** Tài khoản thanh toán · Tài khoản ngoại tệ · Tài khoản thấu chi MyCash · Sinh lời tự động
- **Chi tiêu – Thẻ:** Thẻ tín dụng · Thẻ thanh toán (quốc tế & nội địa)
- **Chi tiêu – Dịch vụ khác:** Chuyển tiền quốc tế · Dịch vụ qua CDM · Đặt lịch hẹn chi nhánh
- **Tiết kiệm:** Tiền gửi tiết kiệm có kỳ hạn · Tích lũy Như Ý · Tiền gửi rút gốc linh hoạt · Chứng chỉ tiền gửi Bảo Lộc
- **Vay mua nhà:** Vay mua nhà dự án trực tiếp từ CĐT · Vay mua BĐS có Giấy chứng nhận · Vay nhận chuyển nhượng
- **Vay mua ô tô:** Vay mua ô tô đi lại
- **Vay tiêu dùng:** MyCash · Vay tín chấp trả góp · Vay cầm cố tiền gửi · Vay xây dựng/sửa chữa nhà · Thấu chi có TSBĐ · Thấu chi không TSBĐ
- **Đầu tư – iBond:** iBond Pro (dòng tiền định sẵn) · iBond Prix (đầu tư linh hoạt) · iBond Prix (tích lũy bền vững)
- **Đầu tư – iFund:** TCBF · TCEF · TCFIN · TCSME · TCRES · TCFF
- **Bảo hiểm sức khỏe:** Song An · Global Prime · An tâm đồng hành · Chăm sóc sức khỏe toàn diện
- **Bảo hiểm tích lũy & đầu tư:** Techcom Life Max Chủ Động · Techcom Life Max Vững Vàng · Khỏe trọn vẹn vượt trội · Khỏe bình an vượt trội · Vững tương lai vượt trội
- **Bảo hiểm khác:** Bảo hiểm nhà tư nhân · Bảo hiểm ô tô · TechCare Travel
- **Ngân hàng số:** Techcombank Mobile · Techcombank Online Banking · Techcombank OneU
