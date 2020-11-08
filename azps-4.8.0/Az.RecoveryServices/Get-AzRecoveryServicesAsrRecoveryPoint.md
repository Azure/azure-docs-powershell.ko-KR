---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047697"
---
# <span data-ttu-id="e6a34-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e6a34-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="e6a34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a34-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a34-103">복제 보호 항목에 대해 사용 가능한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="e6a34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6a34-104">SYNTAX</span></span>

### <span data-ttu-id="e6a34-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6a34-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a34-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e6a34-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6a34-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e6a34-107">DESCRIPTION</span></span>
<span data-ttu-id="e6a34-108">**AzRecoveryServicesAsrRecoveryPoint** cmdlet은 복제 보호 항목에 대해 사용 가능한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="e6a34-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e6a34-109">EXAMPLES</span></span>

### <span data-ttu-id="e6a34-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6a34-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="e6a34-111">지정 된 ASR 복제 보호 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="e6a34-112">변수</span><span class="sxs-lookup"><span data-stu-id="e6a34-112">PARAMETERS</span></span>

### <span data-ttu-id="e6a34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a34-113">-DefaultProfile</span></span>
<span data-ttu-id="e6a34-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e6a34-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e6a34-115">-Name</span></span>
<span data-ttu-id="e6a34-116">가져올 복구 지점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="e6a34-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6a34-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e6a34-118">사용 가능한 복구 지점 목록을 가져올 Azure Site Recovery 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="e6a34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a34-119">CommonParameters</span></span>
<span data-ttu-id="e6a34-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a34-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6a34-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a34-122">입력</span><span class="sxs-lookup"><span data-stu-id="e6a34-122">INPUTS</span></span>

### <span data-ttu-id="e6a34-123">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e6a34-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e6a34-124">출력</span><span class="sxs-lookup"><span data-stu-id="e6a34-124">OUTPUTS</span></span>

### <span data-ttu-id="e6a34-125">SiteRecovery. ASRRecoveryPoint에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e6a34-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="e6a34-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e6a34-126">NOTES</span></span>

## <span data-ttu-id="e6a34-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6a34-127">RELATED LINKS</span></span>

[<span data-ttu-id="e6a34-128">편집-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a34-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e6a34-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a34-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e6a34-130">새로운 AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a34-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e6a34-131">제거-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a34-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e6a34-132">업데이트-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a34-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
