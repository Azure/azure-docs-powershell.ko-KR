---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c5d86909bffa7c38d66c31b56b34a66251b21d65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524315"
---
# <span data-ttu-id="7dc47-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7dc47-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="7dc47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dc47-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc47-103">보호 가능한 항목 목록에 실제 서버를 추가 (검색) 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7dc47-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dc47-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7dc47-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc47-106">**AzureRmRecoveryServicesAsrProtectableItem** 는 ASR 패브릭 내의 보호 컨테이너에 있는 발견 된 보안 가능한 항목 목록에 보호 가능한 새 항목을 추가 합니다 (VMware 패브릭 유형에만 해당).</span><span class="sxs-lookup"><span data-stu-id="7dc47-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="7dc47-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7dc47-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc47-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7dc47-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="7dc47-109">새 Azure Recovery Service ProtectableItem를 추가 하거나 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="7dc47-110">변수</span><span class="sxs-lookup"><span data-stu-id="7dc47-110">PARAMETERS</span></span>

### <span data-ttu-id="7dc47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc47-111">-DefaultProfile</span></span>
<span data-ttu-id="7dc47-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc47-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7dc47-113">-FriendlyName</span></span>
<span data-ttu-id="7dc47-114">보호 가능한 항목의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-114">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="7dc47-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="7dc47-115">-IPAddress</span></span>
<span data-ttu-id="7dc47-116">보호 가능한 항목의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-116">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="7dc47-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="7dc47-117">-OSType</span></span>
<span data-ttu-id="7dc47-118">보호 가능한 항목의 운영 체제 유형 (Windows/Linux)입니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc47-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7dc47-119">-ProtectionContainer</span></span>
<span data-ttu-id="7dc47-120">보호 가능한 항목을 추가 해야 하는 ASR 보호 컨테이너 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc47-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7dc47-121">-Confirm</span></span>
<span data-ttu-id="7dc47-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dc47-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dc47-123">-WhatIf</span></span>
<span data-ttu-id="7dc47-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dc47-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dc47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc47-126">CommonParameters</span></span>
<span data-ttu-id="7dc47-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dc47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc47-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc47-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc47-129">입력</span><span class="sxs-lookup"><span data-stu-id="7dc47-129">INPUTS</span></span>

### <span data-ttu-id="7dc47-130">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="7dc47-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="7dc47-131">출력</span><span class="sxs-lookup"><span data-stu-id="7dc47-131">OUTPUTS</span></span>

### <span data-ttu-id="7dc47-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="7dc47-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7dc47-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7dc47-133">NOTES</span></span>

## <span data-ttu-id="7dc47-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7dc47-134">RELATED LINKS</span></span>
