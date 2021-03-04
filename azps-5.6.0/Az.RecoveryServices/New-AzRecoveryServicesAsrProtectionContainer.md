---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956715"
---
# <span data-ttu-id="5c723-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5c723-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="5c723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c723-102">SYNOPSIS</span></span>
<span data-ttu-id="5c723-103">지정된 패브릭 내에서 Azure Site Recovery Protection Container를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="5c723-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c723-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c723-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c723-105">DESCRIPTION</span></span>
<span data-ttu-id="5c723-106">New-AzRecoveryServicesAsrProtectionContainer cmdlet은 지정된 Azure Site Recovery Fabric 아래에 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="5c723-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c723-107">EXAMPLES</span></span>

### <span data-ttu-id="5c723-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c723-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="5c723-109">지정된 매개 변수를 사용하여 보호 컨테이너 만들기를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5c723-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c723-110">PARAMETERS</span></span>

### <span data-ttu-id="5c723-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c723-111">-DefaultProfile</span></span>
<span data-ttu-id="5c723-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c723-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c723-113">-InputObject</span></span>
<span data-ttu-id="5c723-114">지정된 입력 개체(Azure Fabric)에서 복제 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c723-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5c723-115">-Name</span></span>
<span data-ttu-id="5c723-116">보호 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="5c723-117">-확인</span><span class="sxs-lookup"><span data-stu-id="5c723-117">-Confirm</span></span>
<span data-ttu-id="5c723-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c723-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c723-119">-WhatIf</span></span>
<span data-ttu-id="5c723-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c723-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c723-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c723-122">CommonParameters</span></span>
<span data-ttu-id="5c723-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c723-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c723-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c723-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c723-125">입력</span><span class="sxs-lookup"><span data-stu-id="5c723-125">INPUTS</span></span>

### <span data-ttu-id="5c723-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5c723-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5c723-127">출력</span><span class="sxs-lookup"><span data-stu-id="5c723-127">OUTPUTS</span></span>

### <span data-ttu-id="5c723-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c723-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c723-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c723-129">NOTES</span></span>

## <span data-ttu-id="5c723-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c723-130">RELATED LINKS</span></span>
