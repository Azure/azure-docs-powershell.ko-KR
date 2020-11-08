---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044693"
---
# <span data-ttu-id="92191-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="92191-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="92191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92191-102">SYNOPSIS</span></span>
<span data-ttu-id="92191-103">지정 된 복제 정책을 지정 된 ASR 보호 컨테이너에 연결 하 여 Azure Site Recovery 보호 컨테이너 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92191-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="92191-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92191-104">SYNTAX</span></span>

### <span data-ttu-id="92191-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="92191-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92191-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="92191-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92191-107">설명은</span><span class="sxs-lookup"><span data-stu-id="92191-107">DESCRIPTION</span></span>
<span data-ttu-id="92191-108">**새 AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 복제 정책을 지정 된 보호 컨테이너에 연결 하 여 Azure Site Recovery 보호 컨테이너 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92191-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="92191-109">예제의</span><span class="sxs-lookup"><span data-stu-id="92191-109">EXAMPLES</span></span>

### <span data-ttu-id="92191-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="92191-110">Example 1</span></span>
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

<span data-ttu-id="92191-111">지정 된 매개 변수를 사용 하 여 보호 컨테이너 매핑 만들기를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="92191-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="92191-112">Example 2</span></span>
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

<span data-ttu-id="92191-113">지정 된 매개 변수를 사용 하 여 보호 컨테이너 매핑 만들기를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="92191-114">변수</span><span class="sxs-lookup"><span data-stu-id="92191-114">PARAMETERS</span></span>

### <span data-ttu-id="92191-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92191-115">-DefaultProfile</span></span>
<span data-ttu-id="92191-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92191-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="92191-117">-이름</span><span class="sxs-lookup"><span data-stu-id="92191-117">-Name</span></span>
<span data-ttu-id="92191-118">보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="92191-119">-정책</span><span class="sxs-lookup"><span data-stu-id="92191-119">-Policy</span></span>
<span data-ttu-id="92191-120">매핑에서 사용할 복제 정책에 대 한 ASR 복제 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="92191-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="92191-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="92191-122">매핑에 사용할 기본 보호 컨테이너에 대 한 ASR 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="92191-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="92191-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="92191-124">매핑에 사용할 복구 보호 컨테이너에 대 한 ASR 보호 컨테이너 개체를 지정 합니다 (Azure가 아닌 복구 위치로 복제 하는 경우 사용 됨).</span><span class="sxs-lookup"><span data-stu-id="92191-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="92191-125">-확인</span><span class="sxs-lookup"><span data-stu-id="92191-125">-Confirm</span></span>
<span data-ttu-id="92191-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92191-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92191-127">-WhatIf</span></span>
<span data-ttu-id="92191-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92191-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92191-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92191-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92191-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92191-130">CommonParameters</span></span>
<span data-ttu-id="92191-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92191-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92191-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="92191-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92191-133">입력</span><span class="sxs-lookup"><span data-stu-id="92191-133">INPUTS</span></span>

### <span data-ttu-id="92191-134">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="92191-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="92191-135">출력</span><span class="sxs-lookup"><span data-stu-id="92191-135">OUTPUTS</span></span>

### <span data-ttu-id="92191-136">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="92191-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="92191-137">상속자</span><span class="sxs-lookup"><span data-stu-id="92191-137">NOTES</span></span>

## <span data-ttu-id="92191-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92191-138">RELATED LINKS</span></span>

[<span data-ttu-id="92191-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="92191-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="92191-140">제거-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="92191-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
