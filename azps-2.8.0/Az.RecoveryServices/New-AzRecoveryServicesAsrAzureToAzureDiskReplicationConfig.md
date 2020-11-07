---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872637"
---
# <span data-ttu-id="e04d0-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="e04d0-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e04d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e04d0-103">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="e04d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e04d0-104">SYNTAX</span></span>

### <span data-ttu-id="e04d0-105">AzureToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="e04d0-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e04d0-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e04d0-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e04d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e04d0-107">DESCRIPTION</span></span>
<span data-ttu-id="e04d0-108">디스크를 복제 하는 데 사용 되는 캐시 저장소 계정 및 대상 저장소 계정 (복구 영역)에 Azure 가상 머신 디스크를 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="e04d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e04d0-109">EXAMPLES</span></span>

### <span data-ttu-id="e04d0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e04d0-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="e04d0-111">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다. Azure to Azure EnableDr 및 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="e04d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="e04d0-112">PARAMETERS</span></span>

### <span data-ttu-id="e04d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04d0-113">-DefaultProfile</span></span>
<span data-ttu-id="e04d0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e04d0-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="e04d0-115">-DiskId</span></span>
<span data-ttu-id="e04d0-116">관리 디스크의 디스크 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="e04d0-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e04d0-117">-LogStorageAccountId</span></span>
<span data-ttu-id="e04d0-118">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="e04d0-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e04d0-119">-ManagedDisk</span></span>
<span data-ttu-id="e04d0-120">관리 디스크에 대 한 입력을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="e04d0-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e04d0-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e04d0-122">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="e04d0-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e04d0-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="e04d0-124">복제 된 관리 디스크의 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="e04d0-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e04d0-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e04d0-126">복제 된 관리 디스크에 대 한 복구 리소스 그룹 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="e04d0-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e04d0-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="e04d0-128">복제 된 관리 디스크에 대 한 복구 대상 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="e04d0-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e04d0-129">-VhdUri</span></span>
<span data-ttu-id="e04d0-130">이 매핑이 해당 하는 디스크의 VHD URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="e04d0-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e04d0-131">-Confirm</span></span>
<span data-ttu-id="e04d0-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04d0-133">-WhatIf</span></span>
<span data-ttu-id="e04d0-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e04d0-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e04d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04d0-136">CommonParameters</span></span>
<span data-ttu-id="e04d0-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04d0-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04d0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04d0-139">입력</span><span class="sxs-lookup"><span data-stu-id="e04d0-139">INPUTS</span></span>

### <span data-ttu-id="e04d0-140">않아야</span><span class="sxs-lookup"><span data-stu-id="e04d0-140">None</span></span>

## <span data-ttu-id="e04d0-141">출력</span><span class="sxs-lookup"><span data-stu-id="e04d0-141">OUTPUTS</span></span>

### <span data-ttu-id="e04d0-142">SiteRecovery. ASRAzuretoAzureDiskReplicationConfig에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e04d0-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e04d0-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e04d0-143">NOTES</span></span>

## <span data-ttu-id="e04d0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e04d0-144">RELATED LINKS</span></span>
