---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702105"
---
# <span data-ttu-id="41858-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="41858-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="41858-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41858-102">SYNOPSIS</span></span>
<span data-ttu-id="41858-103">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41858-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41858-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41858-104">SYNTAX</span></span>

### <span data-ttu-id="41858-105">AzureToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="41858-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41858-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="41858-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41858-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41858-107">DESCRIPTION</span></span>
<span data-ttu-id="41858-108">디스크를 복제 하는 데 사용 되는 캐시 저장소 계정 및 대상 저장소 계정 (복구 영역)에 Azure 가상 머신 디스크를 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41858-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="41858-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41858-109">EXAMPLES</span></span>

### <span data-ttu-id="41858-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="41858-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="41858-111">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다. Azure to Azure EnableDr 및 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41858-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="41858-112">변수</span><span class="sxs-lookup"><span data-stu-id="41858-112">PARAMETERS</span></span>

### <span data-ttu-id="41858-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41858-113">-DefaultProfile</span></span>
<span data-ttu-id="41858-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41858-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41858-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="41858-115">-DiskId</span></span>
<span data-ttu-id="41858-116">관리 디스크의 디스크 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41858-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="41858-117">-LogStorageAccountId</span></span>
<span data-ttu-id="41858-118">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="41858-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="41858-119">-ManagedDisk</span></span>
<span data-ttu-id="41858-120">관리 디스크에 대 한 입력을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41858-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="41858-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="41858-122">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="41858-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="41858-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="41858-124">복제 된 관리 디스크의 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41858-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="41858-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="41858-126">복제 된 관리 디스크에 대 한 복구 리소스 그룹 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41858-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="41858-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="41858-128">복제 된 관리 디스크에 대 한 복구 대상 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41858-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="41858-129">-VhdUri</span></span>
<span data-ttu-id="41858-130">이 매핑이 해당 하는 디스크의 VHD URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="41858-131">-확인</span><span class="sxs-lookup"><span data-stu-id="41858-131">-Confirm</span></span>
<span data-ttu-id="41858-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41858-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41858-133">-WhatIf</span></span>
<span data-ttu-id="41858-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41858-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41858-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41858-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41858-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41858-136">CommonParameters</span></span>
<span data-ttu-id="41858-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41858-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41858-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41858-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41858-139">입력</span><span class="sxs-lookup"><span data-stu-id="41858-139">INPUTS</span></span>

### <span data-ttu-id="41858-140">않아야</span><span class="sxs-lookup"><span data-stu-id="41858-140">None</span></span>

## <span data-ttu-id="41858-141">출력</span><span class="sxs-lookup"><span data-stu-id="41858-141">OUTPUTS</span></span>

### <span data-ttu-id="41858-142">SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="41858-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="41858-143">상속자</span><span class="sxs-lookup"><span data-stu-id="41858-143">NOTES</span></span>

## <span data-ttu-id="41858-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41858-144">RELATED LINKS</span></span>
