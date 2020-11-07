---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873474"
---
# <span data-ttu-id="916cb-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="916cb-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="916cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="916cb-102">SYNOPSIS</span></span>
<span data-ttu-id="916cb-103">Rehydrates에 일시 삭제 된 항목</span><span class="sxs-lookup"><span data-stu-id="916cb-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="916cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="916cb-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="916cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="916cb-105">DESCRIPTION</span></span>
<span data-ttu-id="916cb-106">Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates에 일시 삭제 된 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="916cb-107">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="916cb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="916cb-108">EXAMPLES</span></span>

### <span data-ttu-id="916cb-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="916cb-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="916cb-110">첫 번째 명령은 백업 컨테이너의 배열을 가져온 다음 $Cont 배열에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="916cb-111">두 번째 명령에서는 첫 번째 컨테이너 항목에 해당 하는 백업 항목을 가져온 다음 $PI 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="916cb-112">세 번째 명령은 $PI 0에서 항목에 대 한 백업 보호를 사용 하지 않도록 설정 \[ \] 하 고 항목을 소프트 삭제 상태로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="916cb-113">네 번째 명령으로, 소프트 삭제 된 상태의 새 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="916cb-114">마지막 명령은 rehydrates에서 소프트 삭제 된 VM을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="916cb-115">변수</span><span class="sxs-lookup"><span data-stu-id="916cb-115">PARAMETERS</span></span>

### <span data-ttu-id="916cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916cb-116">-DefaultProfile</span></span>
<span data-ttu-id="916cb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="916cb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="916cb-118">-Force</span></span>
<span data-ttu-id="916cb-119">강제로 백업 보호를 사용 하지 않도록 설정 합니다 (확인 대화 상자 방지).</span><span class="sxs-lookup"><span data-stu-id="916cb-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="916cb-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="916cb-121">-항목</span><span class="sxs-lookup"><span data-stu-id="916cb-121">-Item</span></span>
<span data-ttu-id="916cb-122">이 cmdlet이 보호를 해제 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="916cb-123">AzureRmRecoveryServicesBackupItem을 얻으려면 Get-AzRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="916cb-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="916cb-124">-VaultId</span></span>
<span data-ttu-id="916cb-125">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="916cb-126">-확인</span><span class="sxs-lookup"><span data-stu-id="916cb-126">-Confirm</span></span>
<span data-ttu-id="916cb-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="916cb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="916cb-128">-WhatIf</span></span>
<span data-ttu-id="916cb-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="916cb-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="916cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916cb-131">CommonParameters</span></span>
<span data-ttu-id="916cb-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="916cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916cb-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="916cb-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916cb-134">입력</span><span class="sxs-lookup"><span data-stu-id="916cb-134">INPUTS</span></span>

### <span data-ttu-id="916cb-135">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="916cb-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="916cb-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="916cb-136">System.String</span></span>

## <span data-ttu-id="916cb-137">출력</span><span class="sxs-lookup"><span data-stu-id="916cb-137">OUTPUTS</span></span>

### <span data-ttu-id="916cb-138">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="916cb-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="916cb-139">상속자</span><span class="sxs-lookup"><span data-stu-id="916cb-139">NOTES</span></span>

## <span data-ttu-id="916cb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="916cb-140">RELATED LINKS</span></span>

[<span data-ttu-id="916cb-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="916cb-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="916cb-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="916cb-142">Get-AzRecoveryServicesBackupItem</span></span>]()

