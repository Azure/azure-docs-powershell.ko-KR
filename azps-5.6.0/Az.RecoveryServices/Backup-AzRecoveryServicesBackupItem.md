---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3ce18989f737a28cc0949027cb4ea827116b89a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963840"
---
# <span data-ttu-id="d9ad9-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d9ad9-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d9ad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ad9-102">SYNOPSIS</span></span>

<span data-ttu-id="d9ad9-103">백업 항목에 대한 백업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="d9ad9-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9ad9-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ad9-105">설명</span><span class="sxs-lookup"><span data-stu-id="d9ad9-105">DESCRIPTION</span></span>

<span data-ttu-id="d9ad9-106">**Backup-AzRecoveryServicesBackupItem** cmdlet은 보호된 Azure 백업 항목의 추가 백업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="d9ad9-107">이 cmdlet을 사용하면 보호를 사용하도록 설정한 직후에 초기 백업을 수행하거나 예약된 백업이 실패하면 백업을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="d9ad9-108">이 cmdlet은 만료 날짜와 함께 사용자 지정 보존에 사용할 수도 있습니다. 자세한 내용은 매개 변수 도움말 텍스트를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="d9ad9-109">예제</span><span class="sxs-lookup"><span data-stu-id="d9ad9-109">EXAMPLES</span></span>

### <span data-ttu-id="d9ad9-110">예제 1: 백업 항목에 대한 백업 시작</span><span class="sxs-lookup"><span data-stu-id="d9ad9-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="d9ad9-111">첫 번째 명령은 pstestv2vm1이라는 AzureVM 형식의 Backup 컨테이너를 $NamedContainer 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="d9ad9-112">두 번째 명령은 컨테이너에 해당하는 Backup 항목을 $NamedContainer 해당 항목을 $Item 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="d9ad9-113">마지막 명령은 백업 항목의 백업 작업을 $Item.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="d9ad9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d9ad9-114">Example 2</span></span>

<span data-ttu-id="d9ad9-115">백업 항목에 대한 백업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="d9ad9-116">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="d9ad9-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="d9ad9-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d9ad9-117">PARAMETERS</span></span>

### <span data-ttu-id="d9ad9-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="d9ad9-118">-BackupType</span></span>

<span data-ttu-id="d9ad9-119">수행할 백업 유형</span><span class="sxs-lookup"><span data-stu-id="d9ad9-119">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ad9-120">-DefaultProfile</span></span>

<span data-ttu-id="d9ad9-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ad9-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="d9ad9-122">-EnableCompression</span></span>

<span data-ttu-id="d9ad9-123">압축을 사용하도록 설정해야 하는 경우</span><span class="sxs-lookup"><span data-stu-id="d9ad9-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="d9ad9-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="d9ad9-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="d9ad9-125">복구 지점에 대한 만료 시간을 DateTime 개체로 지정합니다. 아무 것도 지정하지 않았다면 기본값은 30일입니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="d9ad9-126">VM, SQL(복사 전용 전체 백업 유형에만 해당), AFS 백업 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad9-127">-항목</span><span class="sxs-lookup"><span data-stu-id="d9ad9-127">-Item</span></span>

<span data-ttu-id="d9ad9-128">이 cmdlet이 백업 작업을 시작하는 Backup 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad9-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d9ad9-129">-VaultId</span></span>

<span data-ttu-id="d9ad9-130">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d9ad9-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d9ad9-131">-Confirm</span></span>

<span data-ttu-id="d9ad9-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ad9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ad9-133">-WhatIf</span></span>

<span data-ttu-id="d9ad9-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="d9ad9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ad9-135">CommonParameters</span></span>
<span data-ttu-id="d9ad9-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ad9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ad9-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9ad9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ad9-138">입력</span><span class="sxs-lookup"><span data-stu-id="d9ad9-138">INPUTS</span></span>

### <span data-ttu-id="d9ad9-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="d9ad9-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d9ad9-140">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9ad9-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d9ad9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ad9-141">System.String</span></span>

## <span data-ttu-id="d9ad9-142">출력</span><span class="sxs-lookup"><span data-stu-id="d9ad9-142">OUTPUTS</span></span>

### <span data-ttu-id="d9ad9-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="d9ad9-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d9ad9-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9ad9-144">NOTES</span></span>

## <span data-ttu-id="d9ad9-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9ad9-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9ad9-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d9ad9-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="d9ad9-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d9ad9-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="d9ad9-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d9ad9-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
