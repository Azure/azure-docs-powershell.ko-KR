---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e9559993e122e5b713228630b3b783b1f0e6a981
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005840"
---
# <span data-ttu-id="cb09c-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cb09c-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="cb09c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb09c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb09c-103">ASR 복제 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="cb09c-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb09c-104">SYNTAX</span></span>

### <span data-ttu-id="cb09c-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb09c-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb09c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cb09c-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb09c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cb09c-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb09c-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb09c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb09c-109">**Get-AzRecoveryServicesAsrPolicy** cmdlet은 구성된 Azure Site Recovery 복제 정책 또는 이름별 특정 복제 정책 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="cb09c-110">예제</span><span class="sxs-lookup"><span data-stu-id="cb09c-110">EXAMPLES</span></span>

### <span data-ttu-id="cb09c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb09c-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="cb09c-112">복제 정책 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="cb09c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cb09c-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="cb09c-114">이름으로 복제 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="cb09c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="cb09c-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="cb09c-116">지정된 친숙한 이름으로 복제 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="cb09c-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb09c-117">PARAMETERS</span></span>

### <span data-ttu-id="cb09c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb09c-118">-DefaultProfile</span></span>
<span data-ttu-id="cb09c-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cb09c-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cb09c-120">-FriendlyName</span></span>
<span data-ttu-id="cb09c-121">ASR 복제 정책의 친숙한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="cb09c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cb09c-122">-Name</span></span>
<span data-ttu-id="cb09c-123">ASR 복제 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="cb09c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb09c-124">CommonParameters</span></span>
<span data-ttu-id="cb09c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb09c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb09c-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb09c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb09c-127">입력</span><span class="sxs-lookup"><span data-stu-id="cb09c-127">INPUTS</span></span>

### <span data-ttu-id="cb09c-128">없음</span><span class="sxs-lookup"><span data-stu-id="cb09c-128">None</span></span>

## <span data-ttu-id="cb09c-129">출력</span><span class="sxs-lookup"><span data-stu-id="cb09c-129">OUTPUTS</span></span>

### <span data-ttu-id="cb09c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="cb09c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="cb09c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb09c-131">NOTES</span></span>

## <span data-ttu-id="cb09c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb09c-132">RELATED LINKS</span></span>

[<span data-ttu-id="cb09c-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cb09c-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="cb09c-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cb09c-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
