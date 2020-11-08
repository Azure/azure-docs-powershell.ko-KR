---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048783"
---
# <span data-ttu-id="e9f2c-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="e9f2c-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e9f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f2c-103">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="e9f2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9f2c-104">SYNTAX</span></span>

### <span data-ttu-id="e9f2c-105">AzureToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="e9f2c-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f2c-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e9f2c-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f2c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e9f2c-107">DESCRIPTION</span></span>
<span data-ttu-id="e9f2c-108">디스크를 복제 하는 데 사용 되는 캐시 저장소 계정 및 대상 저장소 계정 (복구 영역)에 Azure 가상 머신 디스크를 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="e9f2c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e9f2c-109">EXAMPLES</span></span>

### <span data-ttu-id="e9f2c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9f2c-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="e9f2c-111">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다. Azure에서 Azure로 Dr 및 다시 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="e9f2c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9f2c-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="e9f2c-113">복제할 Azure virtual machine 디스크에 대 한 관리 되는 디스크 매핑 개체를 만듭니다. Azure에서 Azure로 Dr 및 다시 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="e9f2c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="e9f2c-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="e9f2c-115">복제할 Azure virtual machine 디스크에 대 한 패스 암호화 설정이 하나인 관리 되는 디스크 매핑 개체를 만듭니다. Azure에서 Azure로 Dr 및 다시 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="e9f2c-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="e9f2c-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="e9f2c-117">대상 디스크 암호화 집합 Id가 포함 된 관리 되는 디스크 매핑 개체를 만들어 복제 될 Azure 가상 머신 디스크에 대해 지정 합니다. Azure에서 Azure로 Dr 및 다시 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="e9f2c-118">변수</span><span class="sxs-lookup"><span data-stu-id="e9f2c-118">PARAMETERS</span></span>

### <span data-ttu-id="e9f2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f2c-119">-DefaultProfile</span></span>
<span data-ttu-id="e9f2c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f2c-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="e9f2c-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="e9f2c-122">디스크 암호화 비밀 url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="e9f2c-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="e9f2c-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="e9f2c-124">디스크 암호화 키 보관소 팔 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="e9f2c-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="e9f2c-125">-DiskId</span></span>
<span data-ttu-id="e9f2c-126">관리 디스크의 디스크 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="e9f2c-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="e9f2c-127">-FailoverDiskName</span></span>
<span data-ttu-id="e9f2c-128">장애 조치 중에 만들어진 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="e9f2c-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e9f2c-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e9f2c-130">키 암호화 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="e9f2c-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="e9f2c-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="e9f2c-132">키 암호화 키 보관소 팔 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="e9f2c-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e9f2c-133">-LogStorageAccountId</span></span>
<span data-ttu-id="e9f2c-134">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="e9f2c-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e9f2c-135">-ManagedDisk</span></span>
<span data-ttu-id="e9f2c-136">관리 디스크에 대 한 입력을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="e9f2c-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e9f2c-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e9f2c-138">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="e9f2c-139">-Recoverydiska Setid</span><span class="sxs-lookup"><span data-stu-id="e9f2c-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="e9f2c-140">복구 디스크에 사용할 Azure 디스크 암호화 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="e9f2c-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e9f2c-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="e9f2c-142">복제 된 관리 디스크의 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-142">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="e9f2c-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e9f2c-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e9f2c-144">복제 된 관리 디스크에 대 한 복구 리소스 그룹 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="e9f2c-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e9f2c-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="e9f2c-146">복제 된 관리 디스크에 대 한 복구 대상 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-146">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="e9f2c-147">-Tdiskname</span><span class="sxs-lookup"><span data-stu-id="e9f2c-147">-TfoDiskName</span></span>
<span data-ttu-id="e9f2c-148">테스트 장애 조치 (failover) 중에 만든 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="e9f2c-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e9f2c-149">-VhdUri</span></span>
<span data-ttu-id="e9f2c-150">이 매핑이 해당 하는 디스크의 VHD URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="e9f2c-151">-확인</span><span class="sxs-lookup"><span data-stu-id="e9f2c-151">-Confirm</span></span>
<span data-ttu-id="e9f2c-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f2c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f2c-153">-WhatIf</span></span>
<span data-ttu-id="e9f2c-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f2c-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f2c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f2c-156">CommonParameters</span></span>
<span data-ttu-id="e9f2c-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f2c-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f2c-159">입력</span><span class="sxs-lookup"><span data-stu-id="e9f2c-159">INPUTS</span></span>

### <span data-ttu-id="e9f2c-160">않아야</span><span class="sxs-lookup"><span data-stu-id="e9f2c-160">None</span></span>

## <span data-ttu-id="e9f2c-161">출력</span><span class="sxs-lookup"><span data-stu-id="e9f2c-161">OUTPUTS</span></span>

### <span data-ttu-id="e9f2c-162">SiteRecovery. ASRAzuretoAzureDiskReplicationConfig에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e9f2c-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e9f2c-163">상속자</span><span class="sxs-lookup"><span data-stu-id="e9f2c-163">NOTES</span></span>

## <span data-ttu-id="e9f2c-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9f2c-164">RELATED LINKS</span></span>
