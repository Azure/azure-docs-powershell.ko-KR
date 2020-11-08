---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212731"
---
# <span data-ttu-id="baa4a-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="baa4a-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="baa4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa4a-102">SYNOPSIS</span></span>
<span data-ttu-id="baa4a-103">ASR 복제 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="baa4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="baa4a-104">SYNTAX</span></span>

### <span data-ttu-id="baa4a-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="baa4a-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa4a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="baa4a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa4a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="baa4a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baa4a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="baa4a-108">DESCRIPTION</span></span>
<span data-ttu-id="baa4a-109">**AzRecoveryServicesAsrPolicy** cmdlet은 구성 된 Azure Site Recovery 복제 정책 또는 이름에 따른 특정 복제 정책의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="baa4a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="baa4a-110">EXAMPLES</span></span>

### <span data-ttu-id="baa4a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="baa4a-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="baa4a-112">복제 정책 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="baa4a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="baa4a-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="baa4a-114">이름이 있는 복제 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="baa4a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="baa4a-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="baa4a-116">지정 된 이름을 가진 복제 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="baa4a-117">변수</span><span class="sxs-lookup"><span data-stu-id="baa4a-117">PARAMETERS</span></span>

### <span data-ttu-id="baa4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa4a-118">-DefaultProfile</span></span>
<span data-ttu-id="baa4a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="baa4a-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="baa4a-120">-FriendlyName</span></span>
<span data-ttu-id="baa4a-121">ASR 복제 정책의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="baa4a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="baa4a-122">-Name</span></span>
<span data-ttu-id="baa4a-123">ASR 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="baa4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa4a-124">CommonParameters</span></span>
<span data-ttu-id="baa4a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa4a-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="baa4a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa4a-127">입력</span><span class="sxs-lookup"><span data-stu-id="baa4a-127">INPUTS</span></span>

### <span data-ttu-id="baa4a-128">않아야</span><span class="sxs-lookup"><span data-stu-id="baa4a-128">None</span></span>

## <span data-ttu-id="baa4a-129">출력</span><span class="sxs-lookup"><span data-stu-id="baa4a-129">OUTPUTS</span></span>

### <span data-ttu-id="baa4a-130">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="baa4a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="baa4a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="baa4a-131">NOTES</span></span>

## <span data-ttu-id="baa4a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="baa4a-132">RELATED LINKS</span></span>

[<span data-ttu-id="baa4a-133">새로운 AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="baa4a-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="baa4a-134">제거-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="baa4a-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
