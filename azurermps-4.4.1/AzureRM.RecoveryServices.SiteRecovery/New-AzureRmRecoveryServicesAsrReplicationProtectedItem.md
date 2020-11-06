---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529200"
---
# <span data-ttu-id="cf273-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf273-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="cf273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf273-102">SYNOPSIS</span></span>
<span data-ttu-id="cf273-103">복제 보호 항목을 만들어 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf273-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf273-104">SYNTAX</span></span>

### <span data-ttu-id="cf273-105">DisableDR (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf273-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf273-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="cf273-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf273-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="cf273-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf273-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="cf273-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf273-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cf273-109">DESCRIPTION</span></span>
<span data-ttu-id="cf273-110">**AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="cf273-111">이 cmdlet을 사용 하 여 ASR 보호 가능한 항목에 대 한 복제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="cf273-112">예제의</span><span class="sxs-lookup"><span data-stu-id="cf273-112">EXAMPLES</span></span>

### <span data-ttu-id="cf273-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf273-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="cf273-114">지정 된 ASR 보호 가능한 항목에 대해 복제 보호 항목 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cf273-115">변수</span><span class="sxs-lookup"><span data-stu-id="cf273-115">PARAMETERS</span></span>

### <span data-ttu-id="cf273-116">-이름</span><span class="sxs-lookup"><span data-stu-id="cf273-116">-Name</span></span>
<span data-ttu-id="cf273-117">ASR 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-118">-OS</span><span class="sxs-lookup"><span data-stu-id="cf273-118">-OS</span></span>
<span data-ttu-id="cf273-119">운영 체제 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-119">Specifies the operating system family.</span></span>
<span data-ttu-id="cf273-120">이 매개 변수에 허용 되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="cf273-121">-OSDiskName</span></span>
<span data-ttu-id="cf273-122">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cf273-123">-ProtectableItem</span></span>
<span data-ttu-id="cf273-124">복제를 사용할 수 있는 ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cf273-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="cf273-126">복제에 사용할 복제 정책에 해당 하는 ASR 보호 컨테이너 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cf273-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="cf273-128">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cf273-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="cf273-130">장애 조치 시 가상 컴퓨터가 생성 될 리소스 그룹의 ARM 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cf273-131">-WaitForCompletion</span></span>
<span data-ttu-id="cf273-132">반환 하기 전에 cmdlet에서 작업이 완료 될 때까지 기다리도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-133">-확인</span><span class="sxs-lookup"><span data-stu-id="cf273-133">-Confirm</span></span>
<span data-ttu-id="cf273-134">작업을 시작 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-134">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf273-135">-WhatIf</span></span>
<span data-ttu-id="cf273-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf273-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf273-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf273-138">CommonParameters</span></span>
<span data-ttu-id="cf273-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf273-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf273-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf273-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf273-141">입력</span><span class="sxs-lookup"><span data-stu-id="cf273-141">INPUTS</span></span>

### <span data-ttu-id="cf273-142">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="cf273-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="cf273-143">출력</span><span class="sxs-lookup"><span data-stu-id="cf273-143">OUTPUTS</span></span>

### <span data-ttu-id="cf273-144">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="cf273-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cf273-145">상속자</span><span class="sxs-lookup"><span data-stu-id="cf273-145">NOTES</span></span>

## <span data-ttu-id="cf273-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf273-146">RELATED LINKS</span></span>

[<span data-ttu-id="cf273-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf273-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cf273-148">제거-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf273-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cf273-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf273-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
