---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046069"
---
# <span data-ttu-id="f0baf-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="f0baf-101">Set-AzureDns</span></span>

## <span data-ttu-id="f0baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0baf-102">SYNOPSIS</span></span>
<span data-ttu-id="f0baf-103">DNS 서버의 IP 주소를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="f0baf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0baf-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f0baf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0baf-105">DESCRIPTION</span></span>
<span data-ttu-id="f0baf-106">**Set AzureDns** Cmdlet은 Azure 서비스에 대 한 DNS 서버의 IP 주소를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="f0baf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0baf-107">EXAMPLES</span></span>

### <span data-ttu-id="f0baf-108">예제 1: DNS 서버의 IP 주소 수정</span><span class="sxs-lookup"><span data-stu-id="f0baf-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="f0baf-109">이 명령은 ContosoService 이라는 서비스에 대해 Dns07 이라는 DNS 서버의 IP 주소를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="f0baf-110">변수</span><span class="sxs-lookup"><span data-stu-id="f0baf-110">PARAMETERS</span></span>

### <span data-ttu-id="f0baf-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f0baf-111">-InformationAction</span></span>
<span data-ttu-id="f0baf-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f0baf-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0baf-114">하기로</span><span class="sxs-lookup"><span data-stu-id="f0baf-114">Continue</span></span>
- <span data-ttu-id="f0baf-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="f0baf-115">Ignore</span></span>
- <span data-ttu-id="f0baf-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f0baf-116">Inquire</span></span>
- <span data-ttu-id="f0baf-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f0baf-117">SilentlyContinue</span></span>
- <span data-ttu-id="f0baf-118">중지가</span><span class="sxs-lookup"><span data-stu-id="f0baf-118">Stop</span></span>
- <span data-ttu-id="f0baf-119">대기</span><span class="sxs-lookup"><span data-stu-id="f0baf-119">Suspend</span></span>

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

### <span data-ttu-id="f0baf-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f0baf-120">-InformationVariable</span></span>
<span data-ttu-id="f0baf-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f0baf-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f0baf-122">-IPAddress</span></span>
<span data-ttu-id="f0baf-123">DNS 서버의 새 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="f0baf-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f0baf-124">-Name</span></span>
<span data-ttu-id="f0baf-125">이 cmdlet이 수정 하는 DNS 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f0baf-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="f0baf-126">-Profile</span></span>
<span data-ttu-id="f0baf-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0baf-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0baf-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f0baf-129">-ServiceName</span></span>
<span data-ttu-id="f0baf-130">이 cmdlet이 DNS 서버의 주소를 수정 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="f0baf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0baf-131">CommonParameters</span></span>
<span data-ttu-id="f0baf-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0baf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0baf-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0baf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0baf-134">입력</span><span class="sxs-lookup"><span data-stu-id="f0baf-134">INPUTS</span></span>

## <span data-ttu-id="f0baf-135">출력</span><span class="sxs-lookup"><span data-stu-id="f0baf-135">OUTPUTS</span></span>

### <span data-ttu-id="f0baf-136">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="f0baf-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="f0baf-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f0baf-137">NOTES</span></span>

## <span data-ttu-id="f0baf-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0baf-138">RELATED LINKS</span></span>

[<span data-ttu-id="f0baf-139">추가-AzureDns</span><span class="sxs-lookup"><span data-stu-id="f0baf-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="f0baf-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="f0baf-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="f0baf-141">새 AzureDns</span><span class="sxs-lookup"><span data-stu-id="f0baf-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="f0baf-142">-AzureDns 제거</span><span class="sxs-lookup"><span data-stu-id="f0baf-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


