---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 934f7ac105ee1164011df9bcacc672437ef4bf78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872798"
---
# <span data-ttu-id="b00a8-101">Disable-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b00a8-101">Disable-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b00a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b00a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b00a8-103">복구 지점의 모든 파일을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-103">Dismounts all the files of the recovery point.</span></span>

## <span data-ttu-id="b00a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b00a8-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b00a8-105">DESCRIPTION</span></span>
<span data-ttu-id="b00a8-106">Disable-AzRecoveryServicesBackupRPMountScript cmdlet은 Get-AzRecoveryServicesBackupRPMountScript cmdlet을 사용 하 여 이전에 탑재 된 복구 지점의 파일을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-106">The Disable-AzRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="b00a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b00a8-107">EXAMPLES</span></span>

### <span data-ttu-id="b00a8-108">예제 1: 복구 지점을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="b00a8-109">변수</span><span class="sxs-lookup"><span data-stu-id="b00a8-109">PARAMETERS</span></span>

### <span data-ttu-id="b00a8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00a8-110">-DefaultProfile</span></span>
<span data-ttu-id="b00a8-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b00a8-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b00a8-112">-PassThru</span></span>
<span data-ttu-id="b00a8-113">복구 지점을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-113">Return the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a8-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b00a8-114">-RecoveryPoint</span></span>
<span data-ttu-id="b00a8-115">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="b00a8-115">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00a8-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b00a8-116">-VaultId</span></span>
<span data-ttu-id="b00a8-117">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b00a8-118">-확인</span><span class="sxs-lookup"><span data-stu-id="b00a8-118">-Confirm</span></span>
<span data-ttu-id="b00a8-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00a8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00a8-120">-WhatIf</span></span>
<span data-ttu-id="b00a8-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00a8-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00a8-123">CommonParameters</span></span>
<span data-ttu-id="b00a8-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b00a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00a8-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00a8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00a8-126">입력</span><span class="sxs-lookup"><span data-stu-id="b00a8-126">INPUTS</span></span>

### <span data-ttu-id="b00a8-127">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="b00a8-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="b00a8-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b00a8-128">System.String</span></span>

## <span data-ttu-id="b00a8-129">출력</span><span class="sxs-lookup"><span data-stu-id="b00a8-129">OUTPUTS</span></span>

### <span data-ttu-id="b00a8-130">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="b00a8-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b00a8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b00a8-131">NOTES</span></span>

## <span data-ttu-id="b00a8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b00a8-132">RELATED LINKS</span></span>
