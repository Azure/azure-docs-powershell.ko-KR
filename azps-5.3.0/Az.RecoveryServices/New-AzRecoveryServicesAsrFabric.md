---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494588"
---
# <span data-ttu-id="b48dc-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b48dc-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="b48dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b48dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b48dc-103">Azure Site Recovery 패브릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="b48dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="b48dc-104">SYNTAX</span></span>

### <span data-ttu-id="b48dc-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="b48dc-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48dc-106">Azure</span><span class="sxs-lookup"><span data-stu-id="b48dc-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b48dc-107">설명</span><span class="sxs-lookup"><span data-stu-id="b48dc-107">DESCRIPTION</span></span>
<span data-ttu-id="b48dc-108">**New-AzRecoveryServicesAsrFabric** cmdlet은 지정된 형식의 Azure Site Recovery Fabric을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="b48dc-109">예제</span><span class="sxs-lookup"><span data-stu-id="b48dc-109">EXAMPLES</span></span>

### <span data-ttu-id="b48dc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b48dc-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="b48dc-111">전달된 이름으로 패브릭 만들기를 시작하고 패브릭 만들기 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="b48dc-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b48dc-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="b48dc-113">전달된 이름으로 Azure 패브릭 만들기를 시작하고 패브릭 만들기 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="b48dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b48dc-114">PARAMETERS</span></span>

### <span data-ttu-id="b48dc-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="b48dc-115">-Azure</span></span>
<span data-ttu-id="b48dc-116">스위치 매개 변수는 Azure 패브릭을 만들기 위해 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48dc-117">-DefaultProfile</span></span>
<span data-ttu-id="b48dc-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b48dc-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b48dc-119">-Location</span></span>
<span data-ttu-id="b48dc-120">생성되는 패브릭 개체에 해당하는 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="b48dc-121">Azure Site Recovery 패브릭 개체는 지역을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="b48dc-122">두 Azure 지역 간에 복제되는 가상 머신의 경우 주 패브릭은 기본 Azure 지역과 복구 패브릭을 나타 내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48dc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b48dc-123">-Name</span></span>
<span data-ttu-id="b48dc-124">Azure Site Recovery Fabric의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="b48dc-125">-Type</span><span class="sxs-lookup"><span data-stu-id="b48dc-125">-Type</span></span>
<span data-ttu-id="b48dc-126">Azure Site Recovery 패브릭 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48dc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b48dc-127">-Confirm</span></span>
<span data-ttu-id="b48dc-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48dc-129">-WhatIf</span></span>
<span data-ttu-id="b48dc-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b48dc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b48dc-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48dc-132">CommonParameters</span></span>
<span data-ttu-id="b48dc-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b48dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48dc-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b48dc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48dc-135">입력</span><span class="sxs-lookup"><span data-stu-id="b48dc-135">INPUTS</span></span>

### <span data-ttu-id="b48dc-136">없음</span><span class="sxs-lookup"><span data-stu-id="b48dc-136">None</span></span>

## <span data-ttu-id="b48dc-137">출력</span><span class="sxs-lookup"><span data-stu-id="b48dc-137">OUTPUTS</span></span>

### <span data-ttu-id="b48dc-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b48dc-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b48dc-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b48dc-139">NOTES</span></span>

## <span data-ttu-id="b48dc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b48dc-140">RELATED LINKS</span></span>

[<span data-ttu-id="b48dc-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b48dc-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="b48dc-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b48dc-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
