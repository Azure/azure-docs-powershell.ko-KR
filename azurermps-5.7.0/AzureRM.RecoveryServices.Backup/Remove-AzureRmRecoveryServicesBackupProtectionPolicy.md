---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526683"
---
# <span data-ttu-id="6c064-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c064-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6c064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c064-102">SYNOPSIS</span></span>
<span data-ttu-id="6c064-103">자격 증명 모음에서 백업 보호 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c064-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c064-104">SYNTAX</span></span>

### <span data-ttu-id="6c064-105">PolicyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6c064-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c064-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="6c064-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c064-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6c064-107">DESCRIPTION</span></span>
<span data-ttu-id="6c064-108">**AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대 한 백업 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="6c064-109">백업 보호 정책을 삭제할 수 있으려면 정책에 연결 된 백업 항목이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="6c064-110">정책을 삭제 하기 전에 연결 된 각 항목이 다른 정책과 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="6c064-111">다른 정책을 백업 항목과 연결 하려면 Enable-AzureRmRecoveryServicesBackupProtection cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="6c064-112">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6c064-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6c064-113">EXAMPLES</span></span>

### <span data-ttu-id="6c064-114">예제 1: 정책 제거</span><span class="sxs-lookup"><span data-stu-id="6c064-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="6c064-115">첫 번째 명령은 NewPolicy 라는 백업 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="6c064-116">두 번째 명령은 $Pol에서 정책 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="6c064-117">변수</span><span class="sxs-lookup"><span data-stu-id="6c064-117">PARAMETERS</span></span>

### <span data-ttu-id="6c064-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c064-118">-DefaultProfile</span></span>
<span data-ttu-id="6c064-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6c064-120">-Force</span></span>
<span data-ttu-id="6c064-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6c064-122">-Name</span></span>
<span data-ttu-id="6c064-123">제거할 백업 보호 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c064-124">-PassThru</span></span>
<span data-ttu-id="6c064-125">삭제할 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-125">Return the policy to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-126">-정책</span><span class="sxs-lookup"><span data-stu-id="6c064-126">-Policy</span></span>
<span data-ttu-id="6c064-127">제거할 백업 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="6c064-128">**Backuppolicy** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6c064-129">-Confirm</span></span>
<span data-ttu-id="6c064-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c064-131">-WhatIf</span></span>
<span data-ttu-id="6c064-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c064-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c064-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c064-134">CommonParameters</span></span>
<span data-ttu-id="6c064-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c064-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c064-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c064-137">입력</span><span class="sxs-lookup"><span data-stu-id="6c064-137">INPUTS</span></span>

### <span data-ttu-id="6c064-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6c064-138">PolicyBase</span></span>
<span data-ttu-id="6c064-139">' Policy ' 매개 변수는 파이프라인에서 ' PolicyBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c064-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="6c064-140">출력</span><span class="sxs-lookup"><span data-stu-id="6c064-140">OUTPUTS</span></span>

## <span data-ttu-id="6c064-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6c064-141">NOTES</span></span>

## <span data-ttu-id="6c064-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c064-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c064-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c064-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6c064-144">새로운 AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c064-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6c064-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c064-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


