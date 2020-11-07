---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: fa308c0961d11320964d7c31a7d77642e968b09b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703317"
---
# <span data-ttu-id="8f0b2-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8f0b2-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="8f0b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0b2-103">사이트 복구에 사이트 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f0b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f0b2-104">SYNTAX</span></span>

### <span data-ttu-id="8f0b2-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f0b2-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f0b2-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8f0b2-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f0b2-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="8f0b2-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f0b2-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="8f0b2-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f0b2-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="8f0b2-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f0b2-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="8f0b2-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f0b2-111">설명은</span><span class="sxs-lookup"><span data-stu-id="8f0b2-111">DESCRIPTION</span></span>
<span data-ttu-id="8f0b2-112">**새 AzureRmSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery에서 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="8f0b2-113">복구 계획은 장애 조치와 복구를 위해 그룹의 가상 컴퓨터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="8f0b2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="8f0b2-114">EXAMPLES</span></span>

### <span data-ttu-id="8f0b2-115">예제 1: 사이트 복구 자격 증명 모음에 복구 계획 추가</span><span class="sxs-lookup"><span data-stu-id="8f0b2-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="8f0b2-116">이 명령은 RecoveryPlan.xml 라는 복구 계획을 Azure Site Recovery 자격 증명 모음에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8f0b2-117">변수</span><span class="sxs-lookup"><span data-stu-id="8f0b2-117">PARAMETERS</span></span>

### <span data-ttu-id="8f0b2-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="8f0b2-118">-Azure</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="8f0b2-119">-FailoverDeploymentModel</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-120">-이름</span><span class="sxs-lookup"><span data-stu-id="8f0b2-120">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-121">-Path</span><span class="sxs-lookup"><span data-stu-id="8f0b2-121">-Path</span></span>
<span data-ttu-id="8f0b2-122">복구 계획 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-122">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-123">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="8f0b2-123">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-124">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="8f0b2-124">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-125">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="8f0b2-125">-PrimarySite</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-126">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="8f0b2-126">-ProtectionEntityList</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-127">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8f0b2-127">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-128">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8f0b2-128">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-129">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8f0b2-129">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0b2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0b2-130">-DefaultProfile</span></span>
<span data-ttu-id="8f0b2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f0b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0b2-132">CommonParameters</span></span>
<span data-ttu-id="8f0b2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0b2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f0b2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0b2-135">입력</span><span class="sxs-lookup"><span data-stu-id="8f0b2-135">INPUTS</span></span>

### <span data-ttu-id="8f0b2-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="8f0b2-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="8f0b2-137">' ProtectionEntityList ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="8f0b2-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="8f0b2-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="8f0b2-139">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f0b2-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="8f0b2-140">출력</span><span class="sxs-lookup"><span data-stu-id="8f0b2-140">OUTPUTS</span></span>

## <span data-ttu-id="8f0b2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8f0b2-141">NOTES</span></span>

## <span data-ttu-id="8f0b2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f0b2-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f0b2-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8f0b2-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="8f0b2-144">제거-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8f0b2-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="8f0b2-145">업데이트-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8f0b2-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


