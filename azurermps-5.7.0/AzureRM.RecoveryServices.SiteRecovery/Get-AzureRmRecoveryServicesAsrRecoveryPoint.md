---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: f5300e120b008540e116596f126e8d2cb9cb2e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528867"
---
# <span data-ttu-id="440f7-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="440f7-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="440f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="440f7-102">SYNOPSIS</span></span>
<span data-ttu-id="440f7-103">복제 보호 항목에 대해 사용 가능한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="440f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="440f7-104">SYNTAX</span></span>

### <span data-ttu-id="440f7-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="440f7-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="440f7-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="440f7-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="440f7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="440f7-107">DESCRIPTION</span></span>
<span data-ttu-id="440f7-108">**AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet은 복제 보호 항목에 대해 사용 가능한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="440f7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="440f7-109">EXAMPLES</span></span>

### <span data-ttu-id="440f7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="440f7-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="440f7-111">지정 된 ASR 복제 보호 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="440f7-112">변수</span><span class="sxs-lookup"><span data-stu-id="440f7-112">PARAMETERS</span></span>

### <span data-ttu-id="440f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440f7-113">-DefaultProfile</span></span>
<span data-ttu-id="440f7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440f7-115">-이름</span><span class="sxs-lookup"><span data-stu-id="440f7-115">-Name</span></span>
<span data-ttu-id="440f7-116">가져올 복구 지점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440f7-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="440f7-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="440f7-118">사용 가능한 복구 지점 목록을 가져올 Azure Site Recovery 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="440f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440f7-119">CommonParameters</span></span>
<span data-ttu-id="440f7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="440f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440f7-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="440f7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440f7-122">입력</span><span class="sxs-lookup"><span data-stu-id="440f7-122">INPUTS</span></span>

### <span data-ttu-id="440f7-123">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="440f7-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="440f7-124">출력</span><span class="sxs-lookup"><span data-stu-id="440f7-124">OUTPUTS</span></span>

### <span data-ttu-id="440f7-125">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRRecoveryPoint, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="440f7-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="440f7-126">상속자</span><span class="sxs-lookup"><span data-stu-id="440f7-126">NOTES</span></span>

## <span data-ttu-id="440f7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="440f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="440f7-128">편집-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440f7-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="440f7-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440f7-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="440f7-130">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440f7-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="440f7-131">제거-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440f7-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="440f7-132">업데이트-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440f7-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
