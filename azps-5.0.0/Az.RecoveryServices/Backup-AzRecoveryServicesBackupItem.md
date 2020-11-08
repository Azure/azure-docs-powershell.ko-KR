---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217554"
---
# <span data-ttu-id="ee77e-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ee77e-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ee77e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee77e-102">SYNOPSIS</span></span>

<span data-ttu-id="ee77e-103">백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="ee77e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee77e-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee77e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee77e-105">DESCRIPTION</span></span>

<span data-ttu-id="ee77e-106">**AzRecoveryServicesBackupItem** cmdlet은 보호 된 Azure 백업 항목의 임시 백업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="ee77e-107">이 cmdlet을 사용 하면 보호를 사용 하도록 설정 하거나 예약 된 백업이 실패할 경우 백업을 시작 하는 즉시 초기 백업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="ee77e-108">이 cmdlet은 만료 날짜가 있거나 없는 사용자 지정 보존에도 사용할 수 있습니다. 자세한 내용은 매개 변수 도움말 텍스트를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee77e-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="ee77e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ee77e-109">EXAMPLES</span></span>

### <span data-ttu-id="ee77e-110">예제 1: 백업 항목에 대 한 백업 시작</span><span class="sxs-lookup"><span data-stu-id="ee77e-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="ee77e-111">첫 번째 명령은 pstestv2vm1 이라는 유형의 Add-azurevm 백업 컨테이너를 가져온 다음이를 $NamedContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="ee77e-112">두 번째 명령은 $NamedContainer의 컨테이너에 해당 하는 백업 항목을 가져온 다음 $Item 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="ee77e-113">마지막 명령은 $Item에서 백업 항목에 대 한 백업 작업을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="ee77e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee77e-114">Example 2</span></span>

<span data-ttu-id="ee77e-115">백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="ee77e-116">생성</span><span class="sxs-lookup"><span data-stu-id="ee77e-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="ee77e-117">변수</span><span class="sxs-lookup"><span data-stu-id="ee77e-117">PARAMETERS</span></span>

### <span data-ttu-id="ee77e-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="ee77e-118">-BackupType</span></span>

<span data-ttu-id="ee77e-119">실행할 백업 유형</span><span class="sxs-lookup"><span data-stu-id="ee77e-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="ee77e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee77e-120">-DefaultProfile</span></span>

<span data-ttu-id="ee77e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee77e-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="ee77e-122">-EnableCompression</span></span>

<span data-ttu-id="ee77e-123">압축을 사용 해야 하는 경우</span><span class="sxs-lookup"><span data-stu-id="ee77e-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="ee77e-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="ee77e-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="ee77e-125">복구 지점의 만료 시간을 DateTime 개체로 지정 합니다. 지정 하지 않은 경우 기본값 30 일이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="ee77e-126">VM, SQL (복사 전용-전체 백업 형식에만 해당), AFS 백업 항목에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="ee77e-127">-항목</span><span class="sxs-lookup"><span data-stu-id="ee77e-127">-Item</span></span>

<span data-ttu-id="ee77e-128">이 cmdlet이 백업 작업을 시작 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="ee77e-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ee77e-129">-VaultId</span></span>

<span data-ttu-id="ee77e-130">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ee77e-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ee77e-131">-Confirm</span></span>

<span data-ttu-id="ee77e-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee77e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee77e-133">-WhatIf</span></span>

<span data-ttu-id="ee77e-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ee77e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee77e-135">CommonParameters</span></span>
<span data-ttu-id="ee77e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee77e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee77e-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee77e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee77e-138">입력</span><span class="sxs-lookup"><span data-stu-id="ee77e-138">INPUTS</span></span>

### <span data-ttu-id="ee77e-139">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="ee77e-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ee77e-140">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ee77e-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ee77e-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee77e-141">System.String</span></span>

## <span data-ttu-id="ee77e-142">출력</span><span class="sxs-lookup"><span data-stu-id="ee77e-142">OUTPUTS</span></span>

### <span data-ttu-id="ee77e-143">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="ee77e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ee77e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ee77e-144">NOTES</span></span>

## <span data-ttu-id="ee77e-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee77e-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee77e-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ee77e-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ee77e-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ee77e-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ee77e-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ee77e-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
