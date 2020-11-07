---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: d0b2d15b3f2515969e423e8ac8d019a1413fcad7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879358"
---
# <span data-ttu-id="1e87d-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1e87d-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="1e87d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e87d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e87d-103">백업 보호 항목에 대 한 보호를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="1e87d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e87d-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e87d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e87d-105">DESCRIPTION</span></span>
<span data-ttu-id="1e87d-106">**AzRecoveryServicesBackupProtection** Cmdlet은 Azure 백업 보호 항목에 대 한 보호를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="1e87d-107">이 cmdlet은 항목의 정기 예약 백업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="1e87d-108">이 cmdlet은 백업 항목에 대 한 기존 복구 지점을 삭제할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="1e87d-109">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1e87d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1e87d-110">EXAMPLES</span></span>

### <span data-ttu-id="1e87d-111">예제 1: 백업 보호 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="1e87d-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="1e87d-112">첫 번째 명령은 백업 컨테이너의 배열을 가져온 다음 $Cont 배열에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="1e87d-113">두 번째 명령에서는 첫 번째 컨테이너 항목에 해당 하는 백업 항목을 가져온 다음 $PI 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="1e87d-114">마지막 명령은 $PI 0에서 항목에 대 한 백업 보호를 사용 하지 않도록 설정 \[ \] 하지만 데이터는 그대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="1e87d-115">변수</span><span class="sxs-lookup"><span data-stu-id="1e87d-115">PARAMETERS</span></span>

### <span data-ttu-id="1e87d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e87d-116">-DefaultProfile</span></span>
<span data-ttu-id="1e87d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e87d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1e87d-118">-Force</span></span>
<span data-ttu-id="1e87d-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e87d-120">-항목</span><span class="sxs-lookup"><span data-stu-id="1e87d-120">-Item</span></span>
<span data-ttu-id="1e87d-121">이 cmdlet이 보호를 해제 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="1e87d-122">**AzureRmRecoveryServicesBackupItem** 을 얻으려면 Get-AzRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="1e87d-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="1e87d-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="1e87d-124">이 cmdlet이 기존 복구 지점을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="1e87d-125">나중에 저장 된 복구 지점을 삭제 하려면이 cmdlet을 다시 실행 하 고이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e87d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1e87d-126">-VaultId</span></span>
<span data-ttu-id="1e87d-127">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1e87d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1e87d-128">-Confirm</span></span>
<span data-ttu-id="1e87d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e87d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e87d-130">-WhatIf</span></span>
<span data-ttu-id="1e87d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e87d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e87d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e87d-133">CommonParameters</span></span>
<span data-ttu-id="1e87d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e87d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e87d-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e87d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e87d-136">입력</span><span class="sxs-lookup"><span data-stu-id="1e87d-136">INPUTS</span></span>

### <span data-ttu-id="1e87d-137">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="1e87d-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="1e87d-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e87d-138">System.String</span></span>

## <span data-ttu-id="1e87d-139">출력</span><span class="sxs-lookup"><span data-stu-id="1e87d-139">OUTPUTS</span></span>

### <span data-ttu-id="1e87d-140">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="1e87d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1e87d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1e87d-141">NOTES</span></span>

## <span data-ttu-id="1e87d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e87d-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e87d-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1e87d-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="1e87d-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1e87d-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="1e87d-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1e87d-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


