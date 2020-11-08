---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7d3b5735cc52ae190cc16c93ad9806a9f47b452d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034075"
---
# <span data-ttu-id="d32b3-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d32b3-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d32b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d32b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d32b3-103">Azure Site Recovery 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="d32b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d32b3-104">SYNTAX</span></span>

### <span data-ttu-id="d32b3-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="d32b3-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d32b3-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d32b3-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d32b3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d32b3-107">DESCRIPTION</span></span>
<span data-ttu-id="d32b3-108">**AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 ASR 보호 컨테이너에 대 한 자격 증명 모음의 복제 정책 매핑 (연결)에 대 한 보호 컨테이너에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="d32b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d32b3-109">EXAMPLES</span></span>

### <span data-ttu-id="d32b3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d32b3-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="d32b3-111">컨테이너에 대 한 보호 컨테이너 매핑 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="d32b3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d32b3-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="d32b3-113">지정 된 보호 컨테이너에 대 한 모든 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="d32b3-114">변수</span><span class="sxs-lookup"><span data-stu-id="d32b3-114">PARAMETERS</span></span>

### <span data-ttu-id="d32b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32b3-115">-DefaultProfile</span></span>
<span data-ttu-id="d32b3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d32b3-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d32b3-117">-Name</span></span>
<span data-ttu-id="d32b3-118">가져올 보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="d32b3-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d32b3-119">-ProtectionContainer</span></span>
<span data-ttu-id="d32b3-120">지정 된 ASR protection 컨테이너 개체에 해당 하는 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d32b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32b3-121">CommonParameters</span></span>
<span data-ttu-id="d32b3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d32b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32b3-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d32b3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32b3-124">입력</span><span class="sxs-lookup"><span data-stu-id="d32b3-124">INPUTS</span></span>

### <span data-ttu-id="d32b3-125">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="d32b3-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d32b3-126">출력</span><span class="sxs-lookup"><span data-stu-id="d32b3-126">OUTPUTS</span></span>

### <span data-ttu-id="d32b3-127">SiteRecovery. ASRProtectionContainerMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="d32b3-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="d32b3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d32b3-128">NOTES</span></span>

## <span data-ttu-id="d32b3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d32b3-129">RELATED LINKS</span></span>

[<span data-ttu-id="d32b3-130">새로운 AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d32b3-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d32b3-131">제거-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d32b3-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
