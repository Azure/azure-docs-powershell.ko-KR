---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 533a5932aea282158bb1f53bf9464942ed9f17c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953195"
---
# <span data-ttu-id="891e8-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="891e8-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="891e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="891e8-102">SYNOPSIS</span></span>
<span data-ttu-id="891e8-103">Azure Site Recovery 복제로 보호된 항목에 대한 복제를 중지/비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="891e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="891e8-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="891e8-105">설명</span><span class="sxs-lookup"><span data-stu-id="891e8-105">DESCRIPTION</span></span>
<span data-ttu-id="891e8-106">**Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정된 Azure Site Recovery 복제 보호 항목의 복제를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="891e8-107">이 작업을 수행하면 보호된 항목에 대한 복제가 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="891e8-108">예제</span><span class="sxs-lookup"><span data-stu-id="891e8-108">EXAMPLES</span></span>

### <span data-ttu-id="891e8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="891e8-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="891e8-110">지정된 복제 보호 항목에 대한 복제 비활성화 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="891e8-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="891e8-111">PARAMETERS</span></span>

### <span data-ttu-id="891e8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891e8-112">-DefaultProfile</span></span>
<span data-ttu-id="891e8-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="891e8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="891e8-114">-Force</span></span>
<span data-ttu-id="891e8-115">추가 경고를 제공하지 않고 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891e8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="891e8-116">-InputObject</span></span>
<span data-ttu-id="891e8-117">cmdlet에 대한 입력 개체: 복제를 사용하지 않도록 설정해야 하는 복제 보호 항목에 해당하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="891e8-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="891e8-118">-WaitForCompletion</span></span>
<span data-ttu-id="891e8-119">cmdlet이 반환하기 전에 작업이 완료될 때까지 기다려야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891e8-120">-확인</span><span class="sxs-lookup"><span data-stu-id="891e8-120">-Confirm</span></span>
<span data-ttu-id="891e8-121">확인이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-121">Specify if confirmation is required.</span></span> <span data-ttu-id="891e8-122">확인을 건너뛰기 위해 확인 매개 변수의 $false 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="891e8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="891e8-123">-WhatIf</span></span>
<span data-ttu-id="891e8-124">cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="891e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891e8-125">CommonParameters</span></span>
<span data-ttu-id="891e8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="891e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891e8-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="891e8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891e8-128">입력</span><span class="sxs-lookup"><span data-stu-id="891e8-128">INPUTS</span></span>

### <span data-ttu-id="891e8-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="891e8-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="891e8-130">출력</span><span class="sxs-lookup"><span data-stu-id="891e8-130">OUTPUTS</span></span>

### <span data-ttu-id="891e8-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="891e8-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="891e8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="891e8-132">NOTES</span></span>

## <span data-ttu-id="891e8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="891e8-133">RELATED LINKS</span></span>

[<span data-ttu-id="891e8-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="891e8-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="891e8-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="891e8-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="891e8-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="891e8-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
