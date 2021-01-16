---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493344"
---
# <span data-ttu-id="2a927-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2a927-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="2a927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a927-102">SYNOPSIS</span></span>
<span data-ttu-id="2a927-103">복제 보호된 항목에 사용 가능한 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="2a927-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a927-104">SYNTAX</span></span>

### <span data-ttu-id="2a927-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="2a927-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a927-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2a927-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a927-107">설명</span><span class="sxs-lookup"><span data-stu-id="2a927-107">DESCRIPTION</span></span>
<span data-ttu-id="2a927-108">**Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet은 복제 보호된 항목에 사용 가능한 복구 지점 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="2a927-109">예제</span><span class="sxs-lookup"><span data-stu-id="2a927-109">EXAMPLES</span></span>

### <span data-ttu-id="2a927-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a927-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="2a927-111">지정된 ASR 복제 보호 항목에 대한 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="2a927-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a927-112">PARAMETERS</span></span>

### <span data-ttu-id="2a927-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a927-113">-DefaultProfile</span></span>
<span data-ttu-id="2a927-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2a927-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2a927-115">-Name</span></span>
<span data-ttu-id="2a927-116">얻을 복구 지점의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a927-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2a927-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2a927-118">사용 가능한 복구 지점 목록을 얻을 Azure Site Recovery 복제 보호된 항목 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a927-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a927-119">CommonParameters</span></span>
<span data-ttu-id="2a927-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a927-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a927-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a927-122">입력</span><span class="sxs-lookup"><span data-stu-id="2a927-122">INPUTS</span></span>

### <span data-ttu-id="2a927-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2a927-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2a927-124">출력</span><span class="sxs-lookup"><span data-stu-id="2a927-124">OUTPUTS</span></span>

### <span data-ttu-id="2a927-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2a927-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="2a927-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a927-126">NOTES</span></span>

## <span data-ttu-id="2a927-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a927-127">RELATED LINKS</span></span>

[<span data-ttu-id="2a927-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a927-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2a927-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a927-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2a927-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a927-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2a927-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a927-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2a927-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a927-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
