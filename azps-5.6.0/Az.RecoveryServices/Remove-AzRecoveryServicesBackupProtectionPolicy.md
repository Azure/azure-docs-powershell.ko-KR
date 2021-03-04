---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 4723fd3087b2f547659e72c1af6b0f5cb7764cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953120"
---
# <span data-ttu-id="1c5d2-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c5d2-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1c5d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5d2-103">자격 증명 모음에서 백업 보호 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="1c5d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c5d2-104">SYNTAX</span></span>

### <span data-ttu-id="1c5d2-105">PolicyName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c5d2-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c5d2-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="1c5d2-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c5d2-107">설명</span><span class="sxs-lookup"><span data-stu-id="1c5d2-107">DESCRIPTION</span></span>
<span data-ttu-id="1c5d2-108">**Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대한 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="1c5d2-109">백업 보호 정책을 삭제하려면 먼저 정책에 연결된 Backup 항목이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="1c5d2-110">정책을 삭제하기 전에 연결된 각 항목이 다른 정책과 연결되어 있는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="1c5d2-111">다른 정책을 Backup 항목과 연결하기 위해 Enable-AzRecoveryServicesBackupProtection cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="1c5d2-112">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1c5d2-113">예제</span><span class="sxs-lookup"><span data-stu-id="1c5d2-113">EXAMPLES</span></span>

### <span data-ttu-id="1c5d2-114">예제 1: 정책 제거</span><span class="sxs-lookup"><span data-stu-id="1c5d2-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="1c5d2-115">첫 번째 명령은 NewPolicy라는 Backup 보호 정책을 구한 다음, 새 변수에 $Pol 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="1c5d2-116">두 번째 명령은 두 번째 명령에서 정책 개체를 $Pol.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="1c5d2-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="1c5d2-117">Example 2</span></span>

<span data-ttu-id="1c5d2-118">자격 증명 모음에서 백업 보호 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="1c5d2-119">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="1c5d2-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="1c5d2-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c5d2-120">PARAMETERS</span></span>

### <span data-ttu-id="1c5d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5d2-121">-DefaultProfile</span></span>
<span data-ttu-id="1c5d2-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c5d2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1c5d2-123">-Force</span></span>
<span data-ttu-id="1c5d2-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c5d2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1c5d2-125">-Name</span></span>
<span data-ttu-id="1c5d2-126">제거할 백업 보호 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="1c5d2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c5d2-127">-PassThru</span></span>
<span data-ttu-id="1c5d2-128">삭제할 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="1c5d2-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="1c5d2-129">-Policy</span></span>
<span data-ttu-id="1c5d2-130">제거할 백업 보호 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="1c5d2-131">**BackupPolicy 개체를 얻은** 경우 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="1c5d2-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1c5d2-132">-VaultId</span></span>
<span data-ttu-id="1c5d2-133">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1c5d2-134">-확인</span><span class="sxs-lookup"><span data-stu-id="1c5d2-134">-Confirm</span></span>
<span data-ttu-id="1c5d2-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c5d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c5d2-136">-WhatIf</span></span>
<span data-ttu-id="1c5d2-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="1c5d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5d2-138">CommonParameters</span></span>
<span data-ttu-id="1c5d2-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c5d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5d2-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c5d2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5d2-141">입력</span><span class="sxs-lookup"><span data-stu-id="1c5d2-141">INPUTS</span></span>

### <span data-ttu-id="1c5d2-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1c5d2-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="1c5d2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1c5d2-143">System.String</span></span>

## <span data-ttu-id="1c5d2-144">출력</span><span class="sxs-lookup"><span data-stu-id="1c5d2-144">OUTPUTS</span></span>

### <span data-ttu-id="1c5d2-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1c5d2-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="1c5d2-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c5d2-146">NOTES</span></span>

## <span data-ttu-id="1c5d2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c5d2-147">RELATED LINKS</span></span>

[<span data-ttu-id="1c5d2-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c5d2-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1c5d2-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c5d2-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1c5d2-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c5d2-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


