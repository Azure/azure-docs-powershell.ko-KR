---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192833"
---
# <span data-ttu-id="a0142-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="a0142-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="a0142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0142-102">SYNOPSIS</span></span>
<span data-ttu-id="a0142-103">부하 분산을 위해 한 프로세스 서버에서 다른 프로세스 서버로 복제를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="a0142-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0142-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0142-105">설명</span><span class="sxs-lookup"><span data-stu-id="a0142-105">DESCRIPTION</span></span>
<span data-ttu-id="a0142-106">**Start-AzRecoveryServicesAsrSwitchProcessServerJob은** 지정된 가상 머신 또는 지정된 프로세스 서버에 대한 복제 데이터 이동을 지정된 대상 프로세스 서버로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="a0142-107">프로세스 서버 간의 부하 분산 또는 복제 전환에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="a0142-108">예제</span><span class="sxs-lookup"><span data-stu-id="a0142-108">EXAMPLES</span></span>

### <span data-ttu-id="a0142-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0142-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="a0142-110">원본에서 대상 프로세스 서버로 모든 복제 보호 항목에 대한 프로세스 서버 전환을 추적하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="a0142-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="a0142-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="a0142-112">원본에서 대상 프로세스 서버로 전달된 복제 보호 항목에 대한 프로세스 서버 전환을 추적하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="a0142-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0142-113">PARAMETERS</span></span>

### <span data-ttu-id="a0142-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0142-114">-DefaultProfile</span></span>
<span data-ttu-id="a0142-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0142-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="a0142-116">-Fabric</span></span>
<span data-ttu-id="a0142-117">구성 서버에 해당하는 Site Recovery 패브릭입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0142-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0142-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a0142-119">프로세스 서버를 전환할 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0142-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="a0142-120">-SourceProcessServer</span></span>
<span data-ttu-id="a0142-121">복제를 전환할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0142-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="a0142-122">-TargetProcessServer</span></span>
<span data-ttu-id="a0142-123">복제를 전환할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0142-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0142-124">-Confirm</span></span>
<span data-ttu-id="a0142-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0142-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0142-126">-WhatIf</span></span>
<span data-ttu-id="a0142-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a0142-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0142-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0142-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0142-129">CommonParameters</span></span>
<span data-ttu-id="a0142-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0142-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0142-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0142-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0142-132">입력</span><span class="sxs-lookup"><span data-stu-id="a0142-132">INPUTS</span></span>

### <span data-ttu-id="a0142-133">없음</span><span class="sxs-lookup"><span data-stu-id="a0142-133">None</span></span>

## <span data-ttu-id="a0142-134">출력</span><span class="sxs-lookup"><span data-stu-id="a0142-134">OUTPUTS</span></span>

### <span data-ttu-id="a0142-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a0142-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a0142-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0142-136">NOTES</span></span>

## <span data-ttu-id="a0142-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0142-137">RELATED LINKS</span></span>
