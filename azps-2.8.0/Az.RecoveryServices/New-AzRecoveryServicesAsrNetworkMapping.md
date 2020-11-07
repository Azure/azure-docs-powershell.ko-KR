---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 0af3ffc25571273ebe572ee315b4e3c97de8f116
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872630"
---
# <span data-ttu-id="f72f0-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f72f0-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="f72f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f72f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f72f0-103">두 네트워크 간에 ASR 네트워크 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="f72f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f72f0-104">SYNTAX</span></span>

### <span data-ttu-id="f72f0-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="f72f0-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f72f0-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f72f0-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f72f0-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f72f0-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f72f0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f72f0-108">DESCRIPTION</span></span>
<span data-ttu-id="f72f0-109">**AzRecoveryServicesAsrNetworkMapping** cmdlet은 두 네트워크 간에 asr 네트워크 매핑을 만드는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 asr 작업의 asr 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f72f0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f72f0-110">EXAMPLES</span></span>

### <span data-ttu-id="f72f0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f72f0-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="f72f0-112">지정 된 이름, 기본 및 복구 네트워크를 사용 하 여 네트워크 매핑 만들기 작업을 시작 하 고 작업을 추적 하는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="f72f0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f72f0-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="f72f0-114">지정 된 이름, 기본 및 복구 네트워크를 사용 하 여 만들기 작업을 위해 네트워크 매핑을 시작 하 고 작업을 추적 하는 ASR 작업을 반환 합니다 (Azure to Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="f72f0-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="f72f0-115">변수</span><span class="sxs-lookup"><span data-stu-id="f72f0-115">PARAMETERS</span></span>

### <span data-ttu-id="f72f0-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f72f0-116">-AzureToAzure</span></span>
<span data-ttu-id="f72f0-117">{{Azureto Fill Toazure 설명}}</span><span class="sxs-lookup"><span data-stu-id="f72f0-117">{{Fill AzureToAzure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72f0-118">-DefaultProfile</span></span>
<span data-ttu-id="f72f0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f72f0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f72f0-120">-Name</span></span>
<span data-ttu-id="f72f0-121">만들 ASR 네트워크 매핑의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="f72f0-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="f72f0-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="f72f0-123">매핑에 대 한 기본 네트워크의 Azure 가상 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="f72f0-124">-PrimaryFabric</span></span>
<span data-ttu-id="f72f0-125">매핑을 만들 ASR 패브릭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="f72f0-126">-PrimaryNetwork</span></span>
<span data-ttu-id="f72f0-127">ASR 네트워크 매핑에 대 한 기본 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="f72f0-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="f72f0-129">네트워크 매핑의 복구 azure 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="f72f0-130">-RecoveryFabric</span></span>
<span data-ttu-id="f72f0-131">복구 Azure 지역에 해당 하는 Azure Site Recovery fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="f72f0-132">-RecoveryNetwork</span></span>
<span data-ttu-id="f72f0-133">ASR 네트워크 매핑에 대 한 복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72f0-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f72f0-134">-Confirm</span></span>
<span data-ttu-id="f72f0-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72f0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f72f0-136">-WhatIf</span></span>
<span data-ttu-id="f72f0-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f72f0-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72f0-139">CommonParameters</span></span>
<span data-ttu-id="f72f0-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f72f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72f0-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72f0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72f0-142">입력</span><span class="sxs-lookup"><span data-stu-id="f72f0-142">INPUTS</span></span>

### <span data-ttu-id="f72f0-143">SiteRecovery. r m/. m g 네트워크</span><span class="sxs-lookup"><span data-stu-id="f72f0-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="f72f0-144">출력</span><span class="sxs-lookup"><span data-stu-id="f72f0-144">OUTPUTS</span></span>

### <span data-ttu-id="f72f0-145">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="f72f0-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f72f0-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f72f0-146">NOTES</span></span>

## <span data-ttu-id="f72f0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f72f0-147">RELATED LINKS</span></span>

[<span data-ttu-id="f72f0-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f72f0-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="f72f0-149">제거-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f72f0-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
