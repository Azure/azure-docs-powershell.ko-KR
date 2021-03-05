---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 0472a24e15a05d1ea07639ee5495efc5feaaba6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987588"
---
# <span data-ttu-id="6bdf0-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6bdf0-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="6bdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdf0-103">지정된 Backup 보호 정책을 사용하여 항목에 대한 백업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="6bdf0-104">구문</span><span class="sxs-lookup"><span data-stu-id="6bdf0-104">SYNTAX</span></span>

### <span data-ttu-id="6bdf0-105">AzureVMComputeEnableProtection(기본값)</span><span class="sxs-lookup"><span data-stu-id="6bdf0-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bdf0-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="6bdf0-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bdf0-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="6bdf0-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bdf0-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="6bdf0-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bdf0-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="6bdf0-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bdf0-110">설명</span><span class="sxs-lookup"><span data-stu-id="6bdf0-110">DESCRIPTION</span></span>
<span data-ttu-id="6bdf0-111">**Enable-AzRecoveryServicesBackupProtection** cmdlet을 사용하면 보호 정책을 항목에 연결하여 백업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="6bdf0-112">정책 ID가 존재하지 않는 경우 또는 백업 항목이 정책과 연결되지 않은 경우 이 명령은 policyID를 예상합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="6bdf0-113">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6bdf0-114">예제</span><span class="sxs-lookup"><span data-stu-id="6bdf0-114">EXAMPLES</span></span>

### <span data-ttu-id="6bdf0-115">예제 1: 항목에 대한 백업 보호 사용</span><span class="sxs-lookup"><span data-stu-id="6bdf0-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="6bdf0-116">첫 번째 cmdlet은 기본 정책 개체를 얻은 다음, $Pol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="6bdf0-117">두 번째 cmdlet은 백업할 디스크 LUNS를 지정하고 백업 변수에 $inclusionDiskLUNS 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="6bdf0-118">세 번째 cmdlet은 ARM V2VM이라는 가상 머신에 대한 백업 보호 정책을 $Pol.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="6bdf0-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="6bdf0-119">Example 2</span></span>

<span data-ttu-id="6bdf0-120">지정된 Backup 보호 정책을 사용하여 항목에 대한 백업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="6bdf0-121">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="6bdf0-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="6bdf0-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6bdf0-122">PARAMETERS</span></span>

### <span data-ttu-id="6bdf0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdf0-123">-DefaultProfile</span></span>
<span data-ttu-id="6bdf0-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bdf0-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="6bdf0-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="6bdf0-126">백업 OS 디스크에만 지정하는 옵션</span><span class="sxs-lookup"><span data-stu-id="6bdf0-126">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="6bdf0-127">-ExclusionDisksList</span></span>
<span data-ttu-id="6bdf0-128">백업에서 제외할 디스크 LUNS 목록과 나머지는 자동으로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="6bdf0-129">-InclusionDisksList</span></span>
<span data-ttu-id="6bdf0-130">백업에 포함될 디스크 LUEN 목록과 나머지는 OS 디스크를 제외한 자동으로 제외됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-131">-항목</span><span class="sxs-lookup"><span data-stu-id="6bdf0-131">-Item</span></span>
<span data-ttu-id="6bdf0-132">이 cmdlet에서 보호를 사용할 수 있는 Backup 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="6bdf0-133">**AzureRmRecoveryServicesBackupItem을** 얻은 경우 Get-AzRecoveryServicesBackupItem cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-134">-Name</span><span class="sxs-lookup"><span data-stu-id="6bdf0-134">-Name</span></span>
<span data-ttu-id="6bdf0-135">Backup 항목의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-135">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-136">-Policy</span><span class="sxs-lookup"><span data-stu-id="6bdf0-136">-Policy</span></span>
<span data-ttu-id="6bdf0-137">이 cmdlet이 항목과 연결되는 보호 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="6bdf0-138">**AzureRmRecoveryServicesBackupProtectionPolicy** 개체를 얻으면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6bdf0-139">-ProtectableItem</span></span>
<span data-ttu-id="6bdf0-140">지정한 정책으로 보호할 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-140">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="6bdf0-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="6bdf0-142">항목과 연결된 디스크 제외 설정을 다시 설정하는 지정</span><span class="sxs-lookup"><span data-stu-id="6bdf0-142">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bdf0-143">-ResourceGroupName</span></span>
<span data-ttu-id="6bdf0-144">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="6bdf0-145">가상 머신에 대해 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-145">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6bdf0-146">-StorageAccountName</span></span>
<span data-ttu-id="6bdf0-147">Azure 파일 공유 저장소 계정 이름</span><span class="sxs-lookup"><span data-stu-id="6bdf0-147">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6bdf0-148">-VaultId</span></span>
<span data-ttu-id="6bdf0-149">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-149">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdf0-150">-확인</span><span class="sxs-lookup"><span data-stu-id="6bdf0-150">-Confirm</span></span>
<span data-ttu-id="6bdf0-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bdf0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdf0-152">-WhatIf</span></span>
<span data-ttu-id="6bdf0-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="6bdf0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdf0-154">CommonParameters</span></span>
<span data-ttu-id="6bdf0-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdf0-156">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bdf0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdf0-157">입력</span><span class="sxs-lookup"><span data-stu-id="6bdf0-157">INPUTS</span></span>

### <span data-ttu-id="6bdf0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="6bdf0-158">System.String</span></span>

### <span data-ttu-id="6bdf0-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="6bdf0-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="6bdf0-160">출력</span><span class="sxs-lookup"><span data-stu-id="6bdf0-160">OUTPUTS</span></span>

### <span data-ttu-id="6bdf0-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="6bdf0-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6bdf0-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6bdf0-162">NOTES</span></span>

## <span data-ttu-id="6bdf0-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bdf0-163">RELATED LINKS</span></span>

[<span data-ttu-id="6bdf0-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6bdf0-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="6bdf0-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6bdf0-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


