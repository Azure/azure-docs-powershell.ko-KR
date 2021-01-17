---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327991"
---
# <span data-ttu-id="02f0f-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="02f0f-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="02f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="02f0f-103">복제 다시동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="02f0f-104">구문</span><span class="sxs-lookup"><span data-stu-id="02f0f-104">SYNTAX</span></span>

### <span data-ttu-id="02f0f-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="02f0f-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f0f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02f0f-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f0f-107">설명</span><span class="sxs-lookup"><span data-stu-id="02f0f-107">DESCRIPTION</span></span>
<span data-ttu-id="02f0f-108">보호된 항목이 다시 동시화 필요한 상태인 경우 **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet은 지정된 보호된 항목에 대한 복제 다시동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="02f0f-109">예제</span><span class="sxs-lookup"><span data-stu-id="02f0f-109">EXAMPLES</span></span>

### <span data-ttu-id="02f0f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="02f0f-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="02f0f-111">전달된 복제 보호된 항목에 대한 복제를 다시동기화하는 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="02f0f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02f0f-112">PARAMETERS</span></span>

### <span data-ttu-id="02f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="02f0f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f0f-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02f0f-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="02f0f-116">복제를 다시동기화하기 위해 ASR 복제 보호된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02f0f-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02f0f-117">-ResourceId</span></span>
<span data-ttu-id="02f0f-118">다시동기화할 복제 보호 항목의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f0f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02f0f-119">-Confirm</span></span>
<span data-ttu-id="02f0f-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f0f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f0f-121">-WhatIf</span></span>
<span data-ttu-id="02f0f-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="02f0f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f0f-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f0f-124">CommonParameters</span></span>
<span data-ttu-id="02f0f-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02f0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f0f-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02f0f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f0f-127">입력</span><span class="sxs-lookup"><span data-stu-id="02f0f-127">INPUTS</span></span>

### <span data-ttu-id="02f0f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="02f0f-128">System.String</span></span>

### <span data-ttu-id="02f0f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02f0f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="02f0f-130">출력</span><span class="sxs-lookup"><span data-stu-id="02f0f-130">OUTPUTS</span></span>

### <span data-ttu-id="02f0f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="02f0f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="02f0f-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02f0f-132">NOTES</span></span>

## <span data-ttu-id="02f0f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02f0f-133">RELATED LINKS</span></span>
