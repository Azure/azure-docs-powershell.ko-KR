---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218025"
---
# <span data-ttu-id="69223-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69223-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="69223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69223-102">SYNOPSIS</span></span>
<span data-ttu-id="69223-103">자격 증명 모음에서 백업 보호 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="69223-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69223-104">SYNTAX</span></span>

### <span data-ttu-id="69223-105">PolicyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="69223-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69223-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="69223-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69223-107">설명은</span><span class="sxs-lookup"><span data-stu-id="69223-107">DESCRIPTION</span></span>
<span data-ttu-id="69223-108">**AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대 한 백업 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="69223-109">백업 보호 정책을 삭제할 수 있으려면 정책에 연결 된 백업 항목이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="69223-110">정책을 삭제 하기 전에 연결 된 각 항목이 다른 정책과 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="69223-111">다른 정책을 백업 항목과 연결 하려면 Enable-AzRecoveryServicesBackupProtection cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="69223-112">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="69223-113">예제의</span><span class="sxs-lookup"><span data-stu-id="69223-113">EXAMPLES</span></span>

### <span data-ttu-id="69223-114">예제 1: 정책 제거</span><span class="sxs-lookup"><span data-stu-id="69223-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="69223-115">첫 번째 명령은 NewPolicy 라는 백업 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="69223-116">두 번째 명령은 $Pol에서 정책 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="69223-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="69223-117">Example 2</span></span>

<span data-ttu-id="69223-118">자격 증명 모음에서 백업 보호 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="69223-119">생성</span><span class="sxs-lookup"><span data-stu-id="69223-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="69223-120">변수</span><span class="sxs-lookup"><span data-stu-id="69223-120">PARAMETERS</span></span>

### <span data-ttu-id="69223-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69223-121">-DefaultProfile</span></span>
<span data-ttu-id="69223-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69223-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69223-123">-Force</span><span class="sxs-lookup"><span data-stu-id="69223-123">-Force</span></span>
<span data-ttu-id="69223-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69223-125">-이름</span><span class="sxs-lookup"><span data-stu-id="69223-125">-Name</span></span>
<span data-ttu-id="69223-126">제거할 백업 보호 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="69223-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69223-127">-PassThru</span></span>
<span data-ttu-id="69223-128">삭제할 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="69223-129">-정책</span><span class="sxs-lookup"><span data-stu-id="69223-129">-Policy</span></span>
<span data-ttu-id="69223-130">제거할 백업 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="69223-131">**Backuppolicy** 개체를 가져오려면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="69223-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="69223-132">-VaultId</span></span>
<span data-ttu-id="69223-133">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69223-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="69223-134">-확인</span><span class="sxs-lookup"><span data-stu-id="69223-134">-Confirm</span></span>
<span data-ttu-id="69223-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69223-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69223-136">-WhatIf</span></span>
<span data-ttu-id="69223-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69223-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="69223-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69223-138">CommonParameters</span></span>
<span data-ttu-id="69223-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69223-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69223-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69223-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69223-141">입력</span><span class="sxs-lookup"><span data-stu-id="69223-141">INPUTS</span></span>

### <span data-ttu-id="69223-142">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="69223-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="69223-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69223-143">System.String</span></span>

## <span data-ttu-id="69223-144">출력</span><span class="sxs-lookup"><span data-stu-id="69223-144">OUTPUTS</span></span>

### <span data-ttu-id="69223-145">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="69223-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="69223-146">상속자</span><span class="sxs-lookup"><span data-stu-id="69223-146">NOTES</span></span>

## <span data-ttu-id="69223-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69223-147">RELATED LINKS</span></span>

[<span data-ttu-id="69223-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69223-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="69223-149">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69223-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="69223-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69223-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


