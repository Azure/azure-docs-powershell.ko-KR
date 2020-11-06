---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 550a8d2a64d4e6f5b887395125daab65d1b551c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533748"
---
# <span data-ttu-id="e0d7a-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d7a-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="e0d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d7a-103">백업 자격 증명 모음에서 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0d7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0d7a-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0d7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0d7a-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d7a-106">**AzureRmBackupProtectionPolicy** Cmdlet은 Azure Backup 자격 증명 모음에서 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="e0d7a-107">백업 보호 정책을 삭제할 수 있으려면 정책에 연결 된 백업 항목이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="e0d7a-108">정책을 삭제 하기 전에 연결 된 각 항목이 다른 정책과 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="e0d7a-109">다른 정책을 백업 항목과 연결 하려면 Enable-AzureRmBackupProtection cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="e0d7a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e0d7a-110">EXAMPLES</span></span>

### <span data-ttu-id="e0d7a-111">예제 1: 백업 보호 정책 제거</span><span class="sxs-lookup"><span data-stu-id="e0d7a-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="e0d7a-112">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="e0d7a-113">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="e0d7a-114">두 번째 명령은 일일 보존 기간에 30 일간 보존 정책을 만든 다음 $Daily 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="e0d7a-115">두 번째 명령은 **AzureRmBackupProtectionPolicy** cmdlet을 사용 하 여 $Vault의 자격 증명 모음에 있는 DailyBackup 이라는 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="e0d7a-116">명령이 현재 cmdlet에 정책을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="e0d7a-117">해당 cmdlet은 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="e0d7a-118">변수</span><span class="sxs-lookup"><span data-stu-id="e0d7a-118">PARAMETERS</span></span>

### <span data-ttu-id="e0d7a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d7a-119">-DefaultProfile</span></span>
<span data-ttu-id="e0d7a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e0d7a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0d7a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e0d7a-121">-Force</span></span>
<span data-ttu-id="e0d7a-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0d7a-123">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d7a-123">-ProtectionPolicy</span></span>
<span data-ttu-id="e0d7a-124">이 cmdlet이 제거 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-124">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="e0d7a-125">**AzureRmBackupProtectionPolicy** 을 얻으려면 Get-AzureRmBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-125">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d7a-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e0d7a-126">-Confirm</span></span>
<span data-ttu-id="e0d7a-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0d7a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d7a-128">-WhatIf</span></span>
<span data-ttu-id="e0d7a-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d7a-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0d7a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d7a-131">CommonParameters</span></span>
<span data-ttu-id="e0d7a-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0d7a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d7a-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d7a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d7a-134">입력</span><span class="sxs-lookup"><span data-stu-id="e0d7a-134">INPUTS</span></span>

### <span data-ttu-id="e0d7a-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d7a-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="e0d7a-136">출력</span><span class="sxs-lookup"><span data-stu-id="e0d7a-136">OUTPUTS</span></span>

### <span data-ttu-id="e0d7a-137">않아야</span><span class="sxs-lookup"><span data-stu-id="e0d7a-137">None</span></span>

## <span data-ttu-id="e0d7a-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e0d7a-138">NOTES</span></span>

## <span data-ttu-id="e0d7a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0d7a-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0d7a-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e0d7a-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="e0d7a-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d7a-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="e0d7a-142">새로운 AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d7a-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


