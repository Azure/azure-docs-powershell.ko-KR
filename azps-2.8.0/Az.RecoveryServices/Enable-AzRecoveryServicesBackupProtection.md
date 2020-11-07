---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872790"
---
# <span data-ttu-id="515a2-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="515a2-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="515a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515a2-102">SYNOPSIS</span></span>
<span data-ttu-id="515a2-103">지정 된 백업 보호 정책이 있는 항목에 대해 백업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="515a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="515a2-104">SYNTAX</span></span>

### <span data-ttu-id="515a2-105">AzureVMComputeEnableProtection (기본값)</span><span class="sxs-lookup"><span data-stu-id="515a2-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515a2-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="515a2-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515a2-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="515a2-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515a2-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="515a2-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515a2-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="515a2-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="515a2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="515a2-110">DESCRIPTION</span></span>
<span data-ttu-id="515a2-111">**AzRecoveryServicesBackupProtection** cmdlet은 항목에 대 한 Azure 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="515a2-112">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="515a2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="515a2-113">EXAMPLES</span></span>

### <span data-ttu-id="515a2-114">예제 1: 항목에 대해 백업 보호 사용</span><span class="sxs-lookup"><span data-stu-id="515a2-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="515a2-115">첫 번째 cmdlet은 기본 정책 개체를 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="515a2-116">두 번째 cmdlet은 $Pol의 정책을 사용 하 여 V2VM 이라는 ARM 가상 컴퓨터에 대 한 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="515a2-117">변수</span><span class="sxs-lookup"><span data-stu-id="515a2-117">PARAMETERS</span></span>

### <span data-ttu-id="515a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515a2-118">-DefaultProfile</span></span>
<span data-ttu-id="515a2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="515a2-120">-항목</span><span class="sxs-lookup"><span data-stu-id="515a2-120">-Item</span></span>
<span data-ttu-id="515a2-121">이 cmdlet이 보호할 수 있는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="515a2-122">**AzureRmRecoveryServicesBackupItem** 을 얻으려면 Get-AzRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="515a2-123">-이름</span><span class="sxs-lookup"><span data-stu-id="515a2-123">-Name</span></span>
<span data-ttu-id="515a2-124">백업 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="515a2-125">-정책</span><span class="sxs-lookup"><span data-stu-id="515a2-125">-Policy</span></span>
<span data-ttu-id="515a2-126">이 cmdlet이 항목과 연결 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="515a2-127">**AzureRmRecoveryServicesBackupProtectionPolicy** 개체를 가져오려면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515a2-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="515a2-128">-ProtectableItem</span></span>
<span data-ttu-id="515a2-129">작업 상태에 대 한 필터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="515a2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515a2-130">-ResourceGroupName</span></span>
<span data-ttu-id="515a2-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="515a2-132">ARM 가상 컴퓨터에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="515a2-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="515a2-133">-ServiceName</span></span>
<span data-ttu-id="515a2-134">서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-134">Specifies the service name.</span></span>
<span data-ttu-id="515a2-135">이 매개 변수는 ASM 가상 머신에만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-135">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="515a2-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="515a2-136">-StorageAccountName</span></span>
<span data-ttu-id="515a2-137">Azure 파일 공유 저장소 계정 이름</span><span class="sxs-lookup"><span data-stu-id="515a2-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="515a2-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="515a2-138">-VaultId</span></span>
<span data-ttu-id="515a2-139">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="515a2-140">-확인</span><span class="sxs-lookup"><span data-stu-id="515a2-140">-Confirm</span></span>
<span data-ttu-id="515a2-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="515a2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515a2-142">-WhatIf</span></span>
<span data-ttu-id="515a2-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="515a2-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="515a2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515a2-145">CommonParameters</span></span>
<span data-ttu-id="515a2-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="515a2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515a2-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="515a2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515a2-148">입력</span><span class="sxs-lookup"><span data-stu-id="515a2-148">INPUTS</span></span>

### <span data-ttu-id="515a2-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="515a2-149">System.String</span></span>

### <span data-ttu-id="515a2-150">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="515a2-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="515a2-151">출력</span><span class="sxs-lookup"><span data-stu-id="515a2-151">OUTPUTS</span></span>

### <span data-ttu-id="515a2-152">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="515a2-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="515a2-153">상속자</span><span class="sxs-lookup"><span data-stu-id="515a2-153">NOTES</span></span>

## <span data-ttu-id="515a2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="515a2-154">RELATED LINKS</span></span>

[<span data-ttu-id="515a2-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="515a2-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="515a2-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="515a2-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


