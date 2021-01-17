---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335882"
---
# <span data-ttu-id="7170f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7170f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7170f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7170f-102">SYNOPSIS</span></span>
<span data-ttu-id="7170f-103">Azure Site Recovery 복제 보호된 항목에 대한 복제를 중지/비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="7170f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7170f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7170f-105">설명</span><span class="sxs-lookup"><span data-stu-id="7170f-105">DESCRIPTION</span></span>
<span data-ttu-id="7170f-106">**Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정된 Azure Site Recovery 복제 보호 항목의 복제를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="7170f-107">이 작업을 수행하면 보호된 항목에 대한 복제가 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="7170f-108">예제</span><span class="sxs-lookup"><span data-stu-id="7170f-108">EXAMPLES</span></span>

### <span data-ttu-id="7170f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7170f-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="7170f-110">지정된 복제 보호 항목에 대한 복제 비활성화 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7170f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7170f-111">PARAMETERS</span></span>

### <span data-ttu-id="7170f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7170f-112">-DefaultProfile</span></span>
<span data-ttu-id="7170f-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7170f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7170f-114">-Force</span></span>
<span data-ttu-id="7170f-115">추가 경고를 제공하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="7170f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7170f-116">-InputObject</span></span>
<span data-ttu-id="7170f-117">cmdlet에 대한 입력 개체: 복제를 비활성화할 복제 보호 항목에 해당하는 ASR 복제 보호된 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="7170f-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7170f-118">-WaitForCompletion</span></span>
<span data-ttu-id="7170f-119">cmdlet이 반환하기 전에 작업이 완료될 때까지 기다려야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="7170f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7170f-120">-Confirm</span></span>
<span data-ttu-id="7170f-121">확인이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-121">Specify if confirmation is required.</span></span> <span data-ttu-id="7170f-122">확인을 건너뛰기 위해 confirm 매개 $false 값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="7170f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7170f-123">-WhatIf</span></span>
<span data-ttu-id="7170f-124">cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떤 일이 일어나는지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="7170f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7170f-125">CommonParameters</span></span>
<span data-ttu-id="7170f-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7170f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7170f-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7170f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7170f-128">입력</span><span class="sxs-lookup"><span data-stu-id="7170f-128">INPUTS</span></span>

### <span data-ttu-id="7170f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7170f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7170f-130">출력</span><span class="sxs-lookup"><span data-stu-id="7170f-130">OUTPUTS</span></span>

### <span data-ttu-id="7170f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7170f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7170f-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7170f-132">NOTES</span></span>

## <span data-ttu-id="7170f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7170f-133">RELATED LINKS</span></span>

[<span data-ttu-id="7170f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7170f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7170f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7170f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7170f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7170f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
