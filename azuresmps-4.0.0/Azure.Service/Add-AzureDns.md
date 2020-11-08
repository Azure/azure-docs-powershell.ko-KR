---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045734"
---
# <span data-ttu-id="0633b-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="0633b-101">Add-AzureDns</span></span>

## <span data-ttu-id="0633b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0633b-102">SYNOPSIS</span></span>
<span data-ttu-id="0633b-103">Azure 서비스에 DNS 서버를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="0633b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0633b-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0633b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0633b-105">DESCRIPTION</span></span>
<span data-ttu-id="0633b-106">**추가-azuredns** CMDLET은 dns 서버를 Azure 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="0633b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0633b-107">EXAMPLES</span></span>

### <span data-ttu-id="0633b-108">예제 1: DNS 서버 추가</span><span class="sxs-lookup"><span data-stu-id="0633b-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="0633b-109">이 명령은 10.1.2.4 주소를 가진 DNS 서버를 ContosoService에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="0633b-110">변수</span><span class="sxs-lookup"><span data-stu-id="0633b-110">PARAMETERS</span></span>

### <span data-ttu-id="0633b-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0633b-111">-InformationAction</span></span>
<span data-ttu-id="0633b-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0633b-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0633b-114">하기로</span><span class="sxs-lookup"><span data-stu-id="0633b-114">Continue</span></span>
- <span data-ttu-id="0633b-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="0633b-115">Ignore</span></span>
- <span data-ttu-id="0633b-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="0633b-116">Inquire</span></span>
- <span data-ttu-id="0633b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0633b-117">SilentlyContinue</span></span>
- <span data-ttu-id="0633b-118">중지가</span><span class="sxs-lookup"><span data-stu-id="0633b-118">Stop</span></span>
- <span data-ttu-id="0633b-119">대기</span><span class="sxs-lookup"><span data-stu-id="0633b-119">Suspend</span></span>

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

### <span data-ttu-id="0633b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0633b-120">-InformationVariable</span></span>
<span data-ttu-id="0633b-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0633b-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0633b-122">-IPAddress</span></span>
<span data-ttu-id="0633b-123">DNS 서버의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-123">Specifies the IP address of the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0633b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="0633b-124">-Name</span></span>
<span data-ttu-id="0633b-125">DNS 서버에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="0633b-126">이 이름은 완전히 정규화 된 도메인 이름이 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-126">This name is not necessarily a fully qualified domain name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0633b-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="0633b-127">-Profile</span></span>
<span data-ttu-id="0633b-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0633b-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0633b-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0633b-130">-ServiceName</span></span>
<span data-ttu-id="0633b-131">이 cmdlet이 DNS 서버를 추가 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0633b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0633b-132">CommonParameters</span></span>
<span data-ttu-id="0633b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0633b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0633b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0633b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0633b-135">입력</span><span class="sxs-lookup"><span data-stu-id="0633b-135">INPUTS</span></span>

## <span data-ttu-id="0633b-136">출력</span><span class="sxs-lookup"><span data-stu-id="0633b-136">OUTPUTS</span></span>

### <span data-ttu-id="0633b-137">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="0633b-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="0633b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0633b-138">NOTES</span></span>

## <span data-ttu-id="0633b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0633b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0633b-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="0633b-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="0633b-141">새 AzureDns</span><span class="sxs-lookup"><span data-stu-id="0633b-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="0633b-142">-AzureDns 제거</span><span class="sxs-lookup"><span data-stu-id="0633b-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="0633b-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="0633b-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


