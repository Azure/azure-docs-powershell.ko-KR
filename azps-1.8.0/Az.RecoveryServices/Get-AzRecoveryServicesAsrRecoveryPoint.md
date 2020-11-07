---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: b381f611d47306c9327d1b276aa3773c34c7b3e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699726"
---
# <span data-ttu-id="27896-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="27896-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="27896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27896-102">SYNOPSIS</span></span>
<span data-ttu-id="27896-103">복제 보호 항목에 대해 사용 가능한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27896-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="27896-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27896-104">SYNTAX</span></span>

### <span data-ttu-id="27896-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="27896-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27896-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="27896-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27896-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27896-107">DESCRIPTION</span></span>
<span data-ttu-id="27896-108">**AzRecoveryServicesAsrRecoveryPoint** cmdlet은 복제 보호 항목에 대해 사용 가능한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27896-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="27896-109">예제의</span><span class="sxs-lookup"><span data-stu-id="27896-109">EXAMPLES</span></span>

### <span data-ttu-id="27896-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="27896-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="27896-111">지정 된 ASR 복제 보호 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27896-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="27896-112">변수</span><span class="sxs-lookup"><span data-stu-id="27896-112">PARAMETERS</span></span>

### <span data-ttu-id="27896-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27896-113">-DefaultProfile</span></span>
<span data-ttu-id="27896-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27896-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="27896-115">-이름</span><span class="sxs-lookup"><span data-stu-id="27896-115">-Name</span></span>
<span data-ttu-id="27896-116">가져올 복구 지점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27896-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="27896-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="27896-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="27896-118">사용 가능한 복구 지점 목록을 가져올 Azure Site Recovery 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27896-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="27896-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27896-119">CommonParameters</span></span>
<span data-ttu-id="27896-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27896-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27896-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27896-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27896-122">입력</span><span class="sxs-lookup"><span data-stu-id="27896-122">INPUTS</span></span>

### <span data-ttu-id="27896-123">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="27896-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="27896-124">출력</span><span class="sxs-lookup"><span data-stu-id="27896-124">OUTPUTS</span></span>

### <span data-ttu-id="27896-125">SiteRecovery. ASRRecoveryPoint에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="27896-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="27896-126">상속자</span><span class="sxs-lookup"><span data-stu-id="27896-126">NOTES</span></span>

## <span data-ttu-id="27896-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27896-127">RELATED LINKS</span></span>

[<span data-ttu-id="27896-128">편집-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27896-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="27896-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27896-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="27896-130">새로운 AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27896-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="27896-131">제거-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27896-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="27896-132">업데이트-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27896-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
