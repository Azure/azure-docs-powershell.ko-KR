---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338601"
---
# <span data-ttu-id="e5a2a-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a2a-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="e5a2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a2a-103">ASR 복제 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="e5a2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5a2a-104">SYNTAX</span></span>

### <span data-ttu-id="e5a2a-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5a2a-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a2a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e5a2a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a2a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5a2a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5a2a-108">설명</span><span class="sxs-lookup"><span data-stu-id="e5a2a-108">DESCRIPTION</span></span>
<span data-ttu-id="e5a2a-109">**Get-AzRecoveryServicesAsrPolicy** cmdlet은 구성된 Azure Site Recovery 복제 정책 또는 이름별 특정 복제 정책 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="e5a2a-110">예제</span><span class="sxs-lookup"><span data-stu-id="e5a2a-110">EXAMPLES</span></span>

### <span data-ttu-id="e5a2a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5a2a-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="e5a2a-112">복제 정책 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="e5a2a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e5a2a-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="e5a2a-114">이름이 있는 복제 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="e5a2a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e5a2a-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="e5a2a-116">지정된 이름의 복제 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="e5a2a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5a2a-117">PARAMETERS</span></span>

### <span data-ttu-id="e5a2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a2a-118">-DefaultProfile</span></span>
<span data-ttu-id="e5a2a-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e5a2a-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5a2a-120">-FriendlyName</span></span>
<span data-ttu-id="e5a2a-121">ASR 복제 정책의 친숙한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="e5a2a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a2a-122">-Name</span></span>
<span data-ttu-id="e5a2a-123">ASR 복제 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="e5a2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a2a-124">CommonParameters</span></span>
<span data-ttu-id="e5a2a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a2a-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5a2a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a2a-127">입력</span><span class="sxs-lookup"><span data-stu-id="e5a2a-127">INPUTS</span></span>

### <span data-ttu-id="e5a2a-128">없음</span><span class="sxs-lookup"><span data-stu-id="e5a2a-128">None</span></span>

## <span data-ttu-id="e5a2a-129">출력</span><span class="sxs-lookup"><span data-stu-id="e5a2a-129">OUTPUTS</span></span>

### <span data-ttu-id="e5a2a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a2a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="e5a2a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5a2a-131">NOTES</span></span>

## <span data-ttu-id="e5a2a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5a2a-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5a2a-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a2a-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="e5a2a-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a2a-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
