---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 696c5812a4b8eece62261208c501727aa48c2262
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042685"
---
# <span data-ttu-id="b0065-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="b0065-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="b0065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0065-102">SYNOPSIS</span></span>
<span data-ttu-id="b0065-103">보호 가능한 항목을 검색 하기 위해 vCenter server를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="b0065-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0065-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0065-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0065-105">DESCRIPTION</span></span>
<span data-ttu-id="b0065-106">**AzRecoveryServicesAsrvCenter** cmdlet은 보호 가능한 항목을 검색 하기 위해 vCenter server를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="b0065-107">이 cmdlet은 구성 서버와 함께 검색을 위해 vCenter server를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="b0065-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b0065-108">EXAMPLES</span></span>

### <span data-ttu-id="b0065-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0065-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="b0065-110">보호 가능한 항목을 검색 하기 위해 vCenter server를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="b0065-111">변수</span><span class="sxs-lookup"><span data-stu-id="b0065-111">PARAMETERS</span></span>

### <span data-ttu-id="b0065-112">-계정</span><span class="sxs-lookup"><span data-stu-id="b0065-112">-Account</span></span>
<span data-ttu-id="b0065-113">사용자 로그인 자격 증명 계정.</span><span class="sxs-lookup"><span data-stu-id="b0065-113">User login credential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0065-114">-DefaultProfile</span></span>
<span data-ttu-id="b0065-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="b0065-116">-Fabric</span></span>
<span data-ttu-id="b0065-117">구성 서버에 해당 하는 ASR 패브릭</span><span class="sxs-lookup"><span data-stu-id="b0065-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-118">-I폰 Hostname</span><span class="sxs-lookup"><span data-stu-id="b0065-118">-IpOrHostName</span></span>
<span data-ttu-id="b0065-119">VCenter server의 IPv4 주소 또는 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b0065-120">-Name</span></span>
<span data-ttu-id="b0065-121">VCenter 서버에 대 한 알기 쉬운 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-122">-포트</span><span class="sxs-lookup"><span data-stu-id="b0065-122">-Port</span></span>
<span data-ttu-id="b0065-123">검색에 사용할 vCenter 서버의 TCP 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-124">-확인</span><span class="sxs-lookup"><span data-stu-id="b0065-124">-Confirm</span></span>
<span data-ttu-id="b0065-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0065-126">-WhatIf</span></span>
<span data-ttu-id="b0065-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0065-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0065-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0065-129">CommonParameters</span></span>
<span data-ttu-id="b0065-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0065-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0065-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0065-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0065-132">입력</span><span class="sxs-lookup"><span data-stu-id="b0065-132">INPUTS</span></span>

### <span data-ttu-id="b0065-133">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="b0065-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b0065-134">출력</span><span class="sxs-lookup"><span data-stu-id="b0065-134">OUTPUTS</span></span>

### <span data-ttu-id="b0065-135">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="b0065-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b0065-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b0065-136">NOTES</span></span>

## <span data-ttu-id="b0065-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0065-137">RELATED LINKS</span></span>
