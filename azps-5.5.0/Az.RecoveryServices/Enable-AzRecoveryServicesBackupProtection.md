---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 41ee67359d4545a5b69ec1f9c44ff8e37302837e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193052"
---
# <span data-ttu-id="7801a-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7801a-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="7801a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7801a-102">SYNOPSIS</span></span>
<span data-ttu-id="7801a-103">지정된 Backup 보호 정책을 사용하여 항목에 대한 백업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="7801a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7801a-104">SYNTAX</span></span>

### <span data-ttu-id="7801a-105">AzureVMComputeEnableProtection(기본값)</span><span class="sxs-lookup"><span data-stu-id="7801a-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7801a-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7801a-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7801a-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7801a-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7801a-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7801a-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7801a-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="7801a-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7801a-110">설명</span><span class="sxs-lookup"><span data-stu-id="7801a-110">DESCRIPTION</span></span>
<span data-ttu-id="7801a-111">**Enable-AzRecoveryServicesBackupProtection** cmdlet은 보호 정책을 항목에 연결하여 백업을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="7801a-112">정책 ID가 존재하지 않는 경우 또는 백업 항목이 정책과 연결되지 않은 경우 이 명령은 policyID를 예상합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="7801a-113">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7801a-114">예제</span><span class="sxs-lookup"><span data-stu-id="7801a-114">EXAMPLES</span></span>

### <span data-ttu-id="7801a-115">예제 1: 항목에 대한 Backup 보호 사용</span><span class="sxs-lookup"><span data-stu-id="7801a-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="7801a-116">첫 번째 cmdlet은 기본 정책 개체를 얻은 다음, $Pol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="7801a-117">두 번째 cmdlet은 백업할 디스크 LUNS를 지정하고 백업 변수에 $inclusionDiskLUNS 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="7801a-118">세 번째 cmdlet은 V2VM이라는 ARM V2VM에 대한 Backup 보호 정책을 $Pol.</span><span class="sxs-lookup"><span data-stu-id="7801a-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="7801a-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="7801a-119">Example 2</span></span>

<span data-ttu-id="7801a-120">지정된 Backup 보호 정책을 사용하여 항목에 대한 백업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="7801a-121">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="7801a-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="7801a-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7801a-122">PARAMETERS</span></span>

### <span data-ttu-id="7801a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7801a-123">-DefaultProfile</span></span>
<span data-ttu-id="7801a-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7801a-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="7801a-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="7801a-126">OS 디스크만 백업하기 위해 지정하는 옵션</span><span class="sxs-lookup"><span data-stu-id="7801a-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="7801a-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="7801a-127">-ExclusionDisksList</span></span>
<span data-ttu-id="7801a-128">백업에서 제외할 디스크 LUNS 목록과 나머지는 자동으로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="7801a-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="7801a-129">-InclusionDisksList</span></span>
<span data-ttu-id="7801a-130">백업에 포함될 디스크 LUNS 목록과 나머지는 OS 디스크를 제외한 자동으로 제외됩니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="7801a-131">-Item</span><span class="sxs-lookup"><span data-stu-id="7801a-131">-Item</span></span>
<span data-ttu-id="7801a-132">이 cmdlet이 보호를 사용할 수 있는 Backup 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="7801a-133">**AzureRmRecoveryServicesBackupItem을** 얻습니다. Get-AzRecoveryServicesBackupItem cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="7801a-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="7801a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7801a-134">-Name</span></span>
<span data-ttu-id="7801a-135">Backup 항목의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="7801a-136">-Policy</span><span class="sxs-lookup"><span data-stu-id="7801a-136">-Policy</span></span>
<span data-ttu-id="7801a-137">이 cmdlet이 항목과 연결되는 보호 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="7801a-138">**AzureRmRecoveryServicesBackupProtectionPolicy** 개체를 얻으면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="7801a-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7801a-139">-ProtectableItem</span></span>
<span data-ttu-id="7801a-140">주어진 정책으로 보호할 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="7801a-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="7801a-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="7801a-142">항목과 연결된 디스크 제외 설정을 다시 설정하는 지정</span><span class="sxs-lookup"><span data-stu-id="7801a-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="7801a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7801a-143">-ResourceGroupName</span></span>
<span data-ttu-id="7801a-144">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="7801a-145">가상 머신에 대해 이 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="7801a-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7801a-146">-StorageAccountName</span></span>
<span data-ttu-id="7801a-147">Azure 파일 공유 저장소 계정 이름</span><span class="sxs-lookup"><span data-stu-id="7801a-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="7801a-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7801a-148">-VaultId</span></span>
<span data-ttu-id="7801a-149">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7801a-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7801a-150">-Confirm</span></span>
<span data-ttu-id="7801a-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7801a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7801a-152">-WhatIf</span></span>
<span data-ttu-id="7801a-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7801a-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="7801a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7801a-154">CommonParameters</span></span>
<span data-ttu-id="7801a-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7801a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7801a-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7801a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7801a-157">입력</span><span class="sxs-lookup"><span data-stu-id="7801a-157">INPUTS</span></span>

### <span data-ttu-id="7801a-158">System.String</span><span class="sxs-lookup"><span data-stu-id="7801a-158">System.String</span></span>

### <span data-ttu-id="7801a-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="7801a-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7801a-160">출력</span><span class="sxs-lookup"><span data-stu-id="7801a-160">OUTPUTS</span></span>

### <span data-ttu-id="7801a-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="7801a-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7801a-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7801a-162">NOTES</span></span>

## <span data-ttu-id="7801a-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7801a-163">RELATED LINKS</span></span>

[<span data-ttu-id="7801a-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7801a-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="7801a-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7801a-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


