---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534604"
---
# <span data-ttu-id="0511b-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0511b-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="0511b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0511b-102">SYNOPSIS</span></span>
<span data-ttu-id="0511b-103">사이트 복구에 사이트 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0511b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0511b-104">SYNTAX</span></span>

### <span data-ttu-id="0511b-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="0511b-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0511b-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="0511b-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0511b-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="0511b-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0511b-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="0511b-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0511b-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="0511b-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0511b-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="0511b-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0511b-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0511b-111">DESCRIPTION</span></span>
<span data-ttu-id="0511b-112">**새 AzureRmSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery에서 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="0511b-113">복구 계획은 장애 조치와 복구를 위해 그룹의 가상 컴퓨터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="0511b-114">예제의</span><span class="sxs-lookup"><span data-stu-id="0511b-114">EXAMPLES</span></span>

### <span data-ttu-id="0511b-115">예제 1: 사이트 복구 자격 증명 모음에 복구 계획 추가</span><span class="sxs-lookup"><span data-stu-id="0511b-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="0511b-116">이 명령은 RecoveryPlan.xml 라는 복구 계획을 Azure Site Recovery 자격 증명 모음에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0511b-117">변수</span><span class="sxs-lookup"><span data-stu-id="0511b-117">PARAMETERS</span></span>

### <span data-ttu-id="0511b-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="0511b-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0511b-119">-DefaultProfile</span></span>
<span data-ttu-id="0511b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0511b-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="0511b-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-122">-이름</span><span class="sxs-lookup"><span data-stu-id="0511b-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-123">-Path</span><span class="sxs-lookup"><span data-stu-id="0511b-123">-Path</span></span>
<span data-ttu-id="0511b-124">복구 계획 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="0511b-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="0511b-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="0511b-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="0511b-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="0511b-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="0511b-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0511b-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0511b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0511b-132">CommonParameters</span></span>
<span data-ttu-id="0511b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0511b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0511b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0511b-135">입력</span><span class="sxs-lookup"><span data-stu-id="0511b-135">INPUTS</span></span>

### <span data-ttu-id="0511b-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="0511b-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="0511b-137">' ProtectionEntityList ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="0511b-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="0511b-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="0511b-139">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0511b-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="0511b-140">출력</span><span class="sxs-lookup"><span data-stu-id="0511b-140">OUTPUTS</span></span>

## <span data-ttu-id="0511b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="0511b-141">NOTES</span></span>

## <span data-ttu-id="0511b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0511b-142">RELATED LINKS</span></span>

[<span data-ttu-id="0511b-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0511b-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="0511b-144">제거-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0511b-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="0511b-145">업데이트-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0511b-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


