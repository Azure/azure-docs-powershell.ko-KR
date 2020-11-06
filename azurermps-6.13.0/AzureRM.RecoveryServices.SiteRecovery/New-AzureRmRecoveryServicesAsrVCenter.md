---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: c27d4d88dd4c2fdf86db5ca39d608add2feb845f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524307"
---
# <span data-ttu-id="1d867-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="1d867-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="1d867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d867-102">SYNOPSIS</span></span>
<span data-ttu-id="1d867-103">보호 가능한 항목을 검색 하기 위해 vCenter server를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d867-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d867-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d867-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d867-105">DESCRIPTION</span></span>
<span data-ttu-id="1d867-106">**AzureRmRecoveryServicesAsrvCenter** cmdlet은 보호 가능한 항목을 검색 하기 위해 vCenter server를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="1d867-107">이 cmdlet은 구성 서버와 함께 검색을 위해 vCenter server를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="1d867-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1d867-108">EXAMPLES</span></span>

### <span data-ttu-id="1d867-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d867-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="1d867-110">보호 가능한 항목을 검색 하기 위해 vCenter server를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="1d867-111">변수</span><span class="sxs-lookup"><span data-stu-id="1d867-111">PARAMETERS</span></span>

### <span data-ttu-id="1d867-112">-계정</span><span class="sxs-lookup"><span data-stu-id="1d867-112">-Account</span></span>
<span data-ttu-id="1d867-113">사용자 로그인 creadential 계정.</span><span class="sxs-lookup"><span data-stu-id="1d867-113">User login creadential Account.</span></span>

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

### <span data-ttu-id="1d867-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d867-114">-DefaultProfile</span></span>
<span data-ttu-id="1d867-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d867-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="1d867-116">-Fabric</span></span>
<span data-ttu-id="1d867-117">구성 서버에 해당 하는 ASR 패브릭</span><span class="sxs-lookup"><span data-stu-id="1d867-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="1d867-118">-I폰 Hostname</span><span class="sxs-lookup"><span data-stu-id="1d867-118">-IpOrHostName</span></span>
<span data-ttu-id="1d867-119">VCenter server의 IPv4 주소 또는 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="1d867-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1d867-120">-Name</span></span>
<span data-ttu-id="1d867-121">VCenter 서버에 대 한 알기 쉬운 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="1d867-122">-포트</span><span class="sxs-lookup"><span data-stu-id="1d867-122">-Port</span></span>
<span data-ttu-id="1d867-123">검색에 사용할 vCenter 서버의 TCP 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="1d867-124">-확인</span><span class="sxs-lookup"><span data-stu-id="1d867-124">-Confirm</span></span>
<span data-ttu-id="1d867-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d867-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d867-126">-WhatIf</span></span>
<span data-ttu-id="1d867-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d867-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d867-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d867-129">CommonParameters</span></span>
<span data-ttu-id="1d867-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d867-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d867-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d867-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d867-132">입력</span><span class="sxs-lookup"><span data-stu-id="1d867-132">INPUTS</span></span>

### <span data-ttu-id="1d867-133">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="1d867-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="1d867-134">출력</span><span class="sxs-lookup"><span data-stu-id="1d867-134">OUTPUTS</span></span>

### <span data-ttu-id="1d867-135">System.webserver. t e r ' 1 [[SiteRecovery Rjob], [[Microsoft Azure. SiteRecovery, Version = 0.1.1.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="1d867-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1d867-136">상속자</span><span class="sxs-lookup"><span data-stu-id="1d867-136">NOTES</span></span>

## <span data-ttu-id="1d867-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d867-137">RELATED LINKS</span></span>
