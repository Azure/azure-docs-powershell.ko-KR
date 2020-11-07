---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699625"
---
# <span data-ttu-id="fcb2d-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcb2d-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="fcb2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb2d-103">자격 증명 모음에서 백업 보호 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="fcb2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcb2d-104">SYNTAX</span></span>

### <span data-ttu-id="fcb2d-105">PolicyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcb2d-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb2d-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="fcb2d-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb2d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcb2d-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb2d-108">**AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대 한 백업 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="fcb2d-109">백업 보호 정책을 삭제할 수 있으려면 정책에 연결 된 백업 항목이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="fcb2d-110">정책을 삭제 하기 전에 연결 된 각 항목이 다른 정책과 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="fcb2d-111">다른 정책을 백업 항목과 연결 하려면 Enable-AzRecoveryServicesBackupProtection cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="fcb2d-112">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fcb2d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="fcb2d-113">EXAMPLES</span></span>

### <span data-ttu-id="fcb2d-114">예제 1: 정책 제거</span><span class="sxs-lookup"><span data-stu-id="fcb2d-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="fcb2d-115">첫 번째 명령은 NewPolicy 라는 백업 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="fcb2d-116">두 번째 명령은 $Pol에서 정책 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="fcb2d-117">변수</span><span class="sxs-lookup"><span data-stu-id="fcb2d-117">PARAMETERS</span></span>

### <span data-ttu-id="fcb2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb2d-118">-DefaultProfile</span></span>
<span data-ttu-id="fcb2d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb2d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fcb2d-120">-Force</span></span>
<span data-ttu-id="fcb2d-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fcb2d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fcb2d-122">-Name</span></span>
<span data-ttu-id="fcb2d-123">제거할 백업 보호 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="fcb2d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcb2d-124">-PassThru</span></span>
<span data-ttu-id="fcb2d-125">삭제할 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="fcb2d-126">-정책</span><span class="sxs-lookup"><span data-stu-id="fcb2d-126">-Policy</span></span>
<span data-ttu-id="fcb2d-127">제거할 백업 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="fcb2d-128">**Backuppolicy** 개체를 가져오려면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="fcb2d-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fcb2d-129">-VaultId</span></span>
<span data-ttu-id="fcb2d-130">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fcb2d-131">-확인</span><span class="sxs-lookup"><span data-stu-id="fcb2d-131">-Confirm</span></span>
<span data-ttu-id="fcb2d-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb2d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb2d-133">-WhatIf</span></span>
<span data-ttu-id="fcb2d-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb2d-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb2d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb2d-136">CommonParameters</span></span>
<span data-ttu-id="fcb2d-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb2d-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb2d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb2d-139">입력</span><span class="sxs-lookup"><span data-stu-id="fcb2d-139">INPUTS</span></span>

### <span data-ttu-id="fcb2d-140">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="fcb2d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcb2d-141">System.String</span></span>

## <span data-ttu-id="fcb2d-142">출력</span><span class="sxs-lookup"><span data-stu-id="fcb2d-142">OUTPUTS</span></span>

### <span data-ttu-id="fcb2d-143">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="fcb2d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="fcb2d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="fcb2d-144">NOTES</span></span>

## <span data-ttu-id="fcb2d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcb2d-145">RELATED LINKS</span></span>

[<span data-ttu-id="fcb2d-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcb2d-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fcb2d-147">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcb2d-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fcb2d-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcb2d-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


