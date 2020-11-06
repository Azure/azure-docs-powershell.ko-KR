---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: aeceb76fe2f1faf6e7e1f2ddf09ee9262370e8ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531955"
---
# <span data-ttu-id="9678d-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9678d-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="9678d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9678d-102">SYNOPSIS</span></span>
<span data-ttu-id="9678d-103">ASR 복제 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9678d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9678d-104">SYNTAX</span></span>

### <span data-ttu-id="9678d-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9678d-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9678d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9678d-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9678d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9678d-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9678d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9678d-108">DESCRIPTION</span></span>
<span data-ttu-id="9678d-109">**AzureRmRecoveryServicesAsrPolicy** cmdlet은 구성 된 Azure Site Recovery 복제 정책 또는 이름에 따른 특정 복제 정책의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="9678d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9678d-110">EXAMPLES</span></span>

### <span data-ttu-id="9678d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9678d-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="9678d-112">복제 정책 목록 Retuns</span><span class="sxs-lookup"><span data-stu-id="9678d-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="9678d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9678d-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="9678d-114">Retuns 복제 정책 (이름)</span><span class="sxs-lookup"><span data-stu-id="9678d-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="9678d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="9678d-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="9678d-116">지정 된 이름을 가진 복제 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="9678d-117">변수</span><span class="sxs-lookup"><span data-stu-id="9678d-117">PARAMETERS</span></span>

### <span data-ttu-id="9678d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9678d-118">-DefaultProfile</span></span>
<span data-ttu-id="9678d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9678d-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9678d-120">-FriendlyName</span></span>
<span data-ttu-id="9678d-121">ASR 복제 정책의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9678d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9678d-122">-Name</span></span>
<span data-ttu-id="9678d-123">ASR 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9678d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9678d-124">CommonParameters</span></span>
<span data-ttu-id="9678d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9678d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9678d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9678d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9678d-127">입력</span><span class="sxs-lookup"><span data-stu-id="9678d-127">INPUTS</span></span>

### <span data-ttu-id="9678d-128">않아야</span><span class="sxs-lookup"><span data-stu-id="9678d-128">None</span></span>

## <span data-ttu-id="9678d-129">출력</span><span class="sxs-lookup"><span data-stu-id="9678d-129">OUTPUTS</span></span>

### <span data-ttu-id="9678d-130">System.webserver. t e r ' 1 [[SiteRecovery], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]],,.</span><span class="sxs-lookup"><span data-stu-id="9678d-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9678d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9678d-131">NOTES</span></span>

## <span data-ttu-id="9678d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9678d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9678d-133">새로운 AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9678d-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="9678d-134">제거-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9678d-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
