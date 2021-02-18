---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192897"
---
# <span data-ttu-id="21717-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="21717-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="21717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21717-102">SYNOPSIS</span></span>
<span data-ttu-id="21717-103">복제할 Azure 가상 머신 디스크에 대한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21717-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="21717-104">구문</span><span class="sxs-lookup"><span data-stu-id="21717-104">SYNTAX</span></span>

### <span data-ttu-id="21717-105">AzureToAzure(기본값)</span><span class="sxs-lookup"><span data-stu-id="21717-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21717-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="21717-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21717-107">설명</span><span class="sxs-lookup"><span data-stu-id="21717-107">DESCRIPTION</span></span>
<span data-ttu-id="21717-108">디스크를 복제하는 데 사용할 캐시 저장소 계정 및 대상 저장소 계정(복구 지역)에 Azure 가상 머신 디스크를 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21717-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="21717-109">예제</span><span class="sxs-lookup"><span data-stu-id="21717-109">EXAMPLES</span></span>

### <span data-ttu-id="21717-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="21717-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="21717-111">복제할 Azure 가상 머신 디스크에 대한 디스크 매핑 개체를 만듭니다. Azure에서 Azure EnableDr로 작업 및 다시 보호 작업 중에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21717-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="21717-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="21717-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="21717-113">복제할 Azure 가상 머신 디스크에 대한 관리 디스크 매핑 개체를 만듭니다. Azure에서 Azure EnableDr로 작업 및 다시 보호 작업 중에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21717-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="21717-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="21717-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="21717-115">복제할 Azure 가상 머신 디스크에 대한 원 패스 암호화 설정을 사용하여 관리 디스크 매핑 개체를 만듭니다. Azure에서 Azure EnableDr로 작업 및 다시 보호 작업 중에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21717-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="21717-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="21717-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="21717-117">Azure 가상 머신 디스크를 복제할 대상 디스크 암호화 집합 ID를 사용하여 관리 디스크 매핑 개체를 만듭니다. Azure에서 Azure EnableDr로 작업 및 다시 보호 작업 중에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21717-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="21717-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21717-118">PARAMETERS</span></span>

### <span data-ttu-id="21717-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21717-119">-DefaultProfile</span></span>
<span data-ttu-id="21717-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21717-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21717-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="21717-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="21717-122">디스크 암호화 비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="21717-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="21717-124">디스크 암호화 키 자격 증명 모음 및 id를 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="21717-125">-DiskId</span></span>
<span data-ttu-id="21717-126">관리 디스크의 디스크 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="21717-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="21717-127">-FailoverDiskName</span></span>
<span data-ttu-id="21717-128">장애 조치(failover) 중에 만든 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="21717-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="21717-130">키 암호화 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="21717-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="21717-132">키 암호화 키 자격 증명 모음 id를 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21717-133">-LogStorageAccountId</span></span>
<span data-ttu-id="21717-134">복제 로그를 저장하는 데 사용할 로그 또는 캐시 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="21717-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="21717-135">-ManagedDisk</span></span>
<span data-ttu-id="21717-136">관리 디스크에 대한 입력을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="21717-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21717-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="21717-138">복제할 Azure 저장소 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="21717-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="21717-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="21717-140">복구 디스크에 사용할 Azure 디스크 암호화 집합의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="21717-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="21717-142">복제된 관리 디스크의 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="21717-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="21717-144">복제된 관리 디스크에 대한 복구 리소스 그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="21717-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="21717-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="21717-146">복제된 관리 디스크에 대한 복구 대상 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="21717-147">-TfoDiskName</span></span>
<span data-ttu-id="21717-148">테스트 장애 조치(failover) 중에 만든 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21717-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="21717-149">-VhdUri</span></span>
<span data-ttu-id="21717-150">이 매핑에 해당하는 디스크의 VHD URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="21717-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21717-151">-Confirm</span></span>
<span data-ttu-id="21717-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21717-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21717-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21717-153">-WhatIf</span></span>
<span data-ttu-id="21717-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="21717-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21717-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21717-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21717-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21717-156">CommonParameters</span></span>
<span data-ttu-id="21717-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21717-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21717-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21717-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21717-159">입력</span><span class="sxs-lookup"><span data-stu-id="21717-159">INPUTS</span></span>

### <span data-ttu-id="21717-160">없음</span><span class="sxs-lookup"><span data-stu-id="21717-160">None</span></span>

## <span data-ttu-id="21717-161">출력</span><span class="sxs-lookup"><span data-stu-id="21717-161">OUTPUTS</span></span>

### <span data-ttu-id="21717-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="21717-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="21717-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21717-163">NOTES</span></span>

## <span data-ttu-id="21717-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21717-164">RELATED LINKS</span></span>
