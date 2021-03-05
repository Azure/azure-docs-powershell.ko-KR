---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f9fe364f680722b1fc34398f0e31a24f53a352ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016144"
---
# <span data-ttu-id="cbd3a-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cbd3a-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="cbd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd3a-103">지정된 복제 정책을 지정된 ASR 보호 컨테이너에 연결하여 Azure Site Recovery Protection Container 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="cbd3a-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbd3a-104">SYNTAX</span></span>

### <span data-ttu-id="cbd3a-105">EnterpriseToAzure(기본값)</span><span class="sxs-lookup"><span data-stu-id="cbd3a-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd3a-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="cbd3a-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd3a-107">설명</span><span class="sxs-lookup"><span data-stu-id="cbd3a-107">DESCRIPTION</span></span>
<span data-ttu-id="cbd3a-108">**New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정된 복제 정책을 지정된 보호 컨테이너에 연결하여 Azure Site Recovery Protection Container 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="cbd3a-109">예제</span><span class="sxs-lookup"><span data-stu-id="cbd3a-109">EXAMPLES</span></span>

### <span data-ttu-id="cbd3a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cbd3a-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="cbd3a-111">지정된 매개 변수를 사용하여 보호 컨테이너 매핑 만들기를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="cbd3a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="cbd3a-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="cbd3a-113">지정된 매개 변수를 사용하여 보호 컨테이너 매핑 만들기를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cbd3a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbd3a-114">PARAMETERS</span></span>

### <span data-ttu-id="cbd3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd3a-115">-DefaultProfile</span></span>
<span data-ttu-id="cbd3a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cbd3a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cbd3a-117">-Name</span></span>
<span data-ttu-id="cbd3a-118">보호 컨테이너 매핑의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-118">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3a-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="cbd3a-119">-Policy</span></span>
<span data-ttu-id="cbd3a-120">매핑에 사용할 복제 정책에 대한 ASR 복제 정책 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3a-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cbd3a-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="cbd3a-122">매핑에 사용할 기본 보호 컨테이너에 대한 ASR 보호 컨테이너 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3a-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cbd3a-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="cbd3a-124">매핑에 사용할 복구 보호 컨테이너에 대한 ASR 보호 컨테이너 개체를 지정합니다(Azure가 아닌 복구 위치에 복제하는 경우 사용됩니다.)</span><span class="sxs-lookup"><span data-stu-id="cbd3a-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3a-125">-확인</span><span class="sxs-lookup"><span data-stu-id="cbd3a-125">-Confirm</span></span>
<span data-ttu-id="cbd3a-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd3a-127">-WhatIf</span></span>
<span data-ttu-id="cbd3a-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbd3a-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd3a-130">CommonParameters</span></span>
<span data-ttu-id="cbd3a-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd3a-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbd3a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd3a-133">입력</span><span class="sxs-lookup"><span data-stu-id="cbd3a-133">INPUTS</span></span>

### <span data-ttu-id="cbd3a-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="cbd3a-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="cbd3a-135">출력</span><span class="sxs-lookup"><span data-stu-id="cbd3a-135">OUTPUTS</span></span>

### <span data-ttu-id="cbd3a-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cbd3a-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cbd3a-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbd3a-137">NOTES</span></span>

## <span data-ttu-id="cbd3a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbd3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="cbd3a-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cbd3a-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="cbd3a-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cbd3a-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
