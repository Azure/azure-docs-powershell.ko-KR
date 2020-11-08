---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045618"
---
# <span data-ttu-id="7b553-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="7b553-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="7b553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b553-102">SYNOPSIS</span></span>
<span data-ttu-id="7b553-103">예약 된 IP 주소를 이름으로 가져오거나 구독에 예약 된 모든 IP 주소를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="7b553-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b553-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7b553-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b553-105">DESCRIPTION</span></span>
<span data-ttu-id="7b553-106">**AzureReservedIP** cmdlet은 이름으로 예약 된 ip 주소를 가져오거나 구독에 예약 된 모든 ip 주소를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="7b553-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7b553-107">EXAMPLES</span></span>

### <span data-ttu-id="7b553-108">예제 1: 모든 예약 된 IP 주소 가져오기</span><span class="sxs-lookup"><span data-stu-id="7b553-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="7b553-109">이 명령은 모든 예약 된 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="7b553-110">예제 2: 지정 된 이름을 사용 하 여 예약 된 IP 주소 가져오기</span><span class="sxs-lookup"><span data-stu-id="7b553-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="7b553-111">이 명령은 $IpName 변수로 지정 된 이름이 있는 예약 된 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="7b553-112">변수</span><span class="sxs-lookup"><span data-stu-id="7b553-112">PARAMETERS</span></span>

### <span data-ttu-id="7b553-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7b553-113">-InformationAction</span></span>
<span data-ttu-id="7b553-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7b553-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b553-116">하기로</span><span class="sxs-lookup"><span data-stu-id="7b553-116">Continue</span></span>
- <span data-ttu-id="7b553-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="7b553-117">Ignore</span></span>
- <span data-ttu-id="7b553-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="7b553-118">Inquire</span></span>
- <span data-ttu-id="7b553-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7b553-119">SilentlyContinue</span></span>
- <span data-ttu-id="7b553-120">중지가</span><span class="sxs-lookup"><span data-stu-id="7b553-120">Stop</span></span>
- <span data-ttu-id="7b553-121">대기</span><span class="sxs-lookup"><span data-stu-id="7b553-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b553-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7b553-122">-InformationVariable</span></span>
<span data-ttu-id="7b553-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b553-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="7b553-124">-Profile</span></span>
<span data-ttu-id="7b553-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7b553-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b553-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="7b553-127">-ReservedIPName</span></span>
<span data-ttu-id="7b553-128">예약 된 IP 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b553-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b553-129">CommonParameters</span></span>
<span data-ttu-id="7b553-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b553-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b553-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b553-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b553-132">입력</span><span class="sxs-lookup"><span data-stu-id="7b553-132">INPUTS</span></span>

## <span data-ttu-id="7b553-133">출력</span><span class="sxs-lookup"><span data-stu-id="7b553-133">OUTPUTS</span></span>

## <span data-ttu-id="7b553-134">상속자</span><span class="sxs-lookup"><span data-stu-id="7b553-134">NOTES</span></span>

## <span data-ttu-id="7b553-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b553-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b553-136">새로운 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="7b553-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="7b553-137">제거-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="7b553-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


