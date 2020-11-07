---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c893d256351473aa1d840cf1a7e62a960300bdf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702295"
---
# <span data-ttu-id="b9bbd-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b9bbd-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="b9bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bbd-103">Azure Site Recovery 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9bbd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9bbd-104">SYNTAX</span></span>

### <span data-ttu-id="b9bbd-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9bbd-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9bbd-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b9bbd-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9bbd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b9bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="b9bbd-108">**AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 ASR 보호 컨테이너에 대 한 자격 증명 모음의 복제 정책 매핑 (연결)에 대 한 보호 컨테이너에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="b9bbd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b9bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="b9bbd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9bbd-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="b9bbd-111">컨테이너에 대 한 보호 컨테이너 매핑 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="b9bbd-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b9bbd-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

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

<span data-ttu-id="b9bbd-113">지정 된 보호 컨테이너에 대 한 모든 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="b9bbd-114">변수</span><span class="sxs-lookup"><span data-stu-id="b9bbd-114">PARAMETERS</span></span>

### <span data-ttu-id="b9bbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bbd-115">-DefaultProfile</span></span>
<span data-ttu-id="b9bbd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b9bbd-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b9bbd-117">-Name</span></span>
<span data-ttu-id="b9bbd-118">가져올 보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="b9bbd-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b9bbd-119">-ProtectionContainer</span></span>
<span data-ttu-id="b9bbd-120">지정 된 ASR protection 컨테이너 개체에 해당 하는 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="b9bbd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bbd-121">CommonParameters</span></span>
<span data-ttu-id="b9bbd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bbd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bbd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bbd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bbd-124">입력</span><span class="sxs-lookup"><span data-stu-id="b9bbd-124">INPUTS</span></span>

### <span data-ttu-id="b9bbd-125">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="b9bbd-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="b9bbd-126">출력</span><span class="sxs-lookup"><span data-stu-id="b9bbd-126">OUTPUTS</span></span>

### <span data-ttu-id="b9bbd-127">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectionContainerMapping, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="b9bbd-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b9bbd-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b9bbd-128">NOTES</span></span>

## <span data-ttu-id="b9bbd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9bbd-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9bbd-130">새로운 AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b9bbd-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="b9bbd-131">제거-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b9bbd-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
