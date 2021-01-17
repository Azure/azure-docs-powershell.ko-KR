---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491694"
---
# <span data-ttu-id="7af4c-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af4c-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="7af4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7af4c-102">SYNOPSIS</span></span>
<span data-ttu-id="7af4c-103">자격 증명 모음에서 Backup 보호 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="7af4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7af4c-104">SYNTAX</span></span>

### <span data-ttu-id="7af4c-105">PolicyName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7af4c-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7af4c-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="7af4c-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7af4c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7af4c-107">DESCRIPTION</span></span>
<span data-ttu-id="7af4c-108">**Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대한 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="7af4c-109">Backup 보호 정책을 삭제하려면 먼저 정책에 연결된 Backup 항목이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="7af4c-110">정책을 삭제하기 전에 연결된 각 항목이 다른 정책과 연결되어 있는지를 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="7af4c-111">다른 정책을 Backup 항목과 연결하기 위해 Enable-AzRecoveryServicesBackupProtection cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="7af4c-112">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7af4c-113">예제</span><span class="sxs-lookup"><span data-stu-id="7af4c-113">EXAMPLES</span></span>

### <span data-ttu-id="7af4c-114">예제 1: 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7af4c-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="7af4c-115">첫 번째 명령은 NewPolicy라는 Backup 보호 정책을 $Pol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="7af4c-116">두 번째 명령은 다음 명령에서 정책 개체를 $Pol.</span><span class="sxs-lookup"><span data-stu-id="7af4c-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="7af4c-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="7af4c-117">Example 2</span></span>

<span data-ttu-id="7af4c-118">자격 증명 모음에서 Backup 보호 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="7af4c-119">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="7af4c-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="7af4c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7af4c-120">PARAMETERS</span></span>

### <span data-ttu-id="7af4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af4c-121">-DefaultProfile</span></span>
<span data-ttu-id="7af4c-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7af4c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7af4c-123">-Force</span></span>
<span data-ttu-id="7af4c-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af4c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7af4c-125">-Name</span></span>
<span data-ttu-id="7af4c-126">제거할 Backup 보호 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af4c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7af4c-127">-PassThru</span></span>
<span data-ttu-id="7af4c-128">삭제할 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-128">Return the policy to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af4c-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="7af4c-129">-Policy</span></span>
<span data-ttu-id="7af4c-130">제거할 Backup 보호 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="7af4c-131">**BackupPolicy** 개체를 얻습니다. Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7af4c-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7af4c-132">-VaultId</span></span>
<span data-ttu-id="7af4c-133">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7af4c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7af4c-134">-Confirm</span></span>
<span data-ttu-id="7af4c-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af4c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7af4c-136">-WhatIf</span></span>
<span data-ttu-id="7af4c-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7af4c-137">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af4c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af4c-138">CommonParameters</span></span>
<span data-ttu-id="7af4c-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7af4c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af4c-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7af4c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af4c-141">입력</span><span class="sxs-lookup"><span data-stu-id="7af4c-141">INPUTS</span></span>

### <span data-ttu-id="7af4c-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="7af4c-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="7af4c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7af4c-143">System.String</span></span>

## <span data-ttu-id="7af4c-144">출력</span><span class="sxs-lookup"><span data-stu-id="7af4c-144">OUTPUTS</span></span>

### <span data-ttu-id="7af4c-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="7af4c-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="7af4c-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7af4c-146">NOTES</span></span>

## <span data-ttu-id="7af4c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7af4c-147">RELATED LINKS</span></span>

[<span data-ttu-id="7af4c-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af4c-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7af4c-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af4c-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7af4c-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af4c-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


