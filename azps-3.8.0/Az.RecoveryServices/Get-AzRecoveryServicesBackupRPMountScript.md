---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 427da45eed5e2e9e27421e67d9e6e776d9106367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044731"
---
# <span data-ttu-id="6eacd-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="6eacd-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="6eacd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eacd-102">SYNOPSIS</span></span>
<span data-ttu-id="6eacd-103">복구 지점의 모든 파일을 탑재 하는 스크립트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="6eacd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6eacd-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eacd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6eacd-105">DESCRIPTION</span></span>
<span data-ttu-id="6eacd-106">Get-AzRecoveryServicesBackupRPMountScript cmdlet은 앱이 실행 되는 컴퓨터에 복구 지점의 볼륨을 탑재 하는 스크립트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="6eacd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6eacd-107">EXAMPLES</span></span>

### <span data-ttu-id="6eacd-108">예제 1: 복구 지점을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-108">Example 1: Mount a recovery point</span></span>
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
```

<span data-ttu-id="6eacd-109">스크립트를 실행 하면 복구 지점의 파일이 $rp 0이 탑재 됩니다. \[\]</span><span class="sxs-lookup"><span data-stu-id="6eacd-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="6eacd-110">변수</span><span class="sxs-lookup"><span data-stu-id="6eacd-110">PARAMETERS</span></span>

### <span data-ttu-id="6eacd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eacd-111">-DefaultProfile</span></span>
<span data-ttu-id="6eacd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eacd-113">-Path</span><span class="sxs-lookup"><span data-stu-id="6eacd-113">-Path</span></span>
<span data-ttu-id="6eacd-114">파일을 복구 하는 경우 파일을 다운로드할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="6eacd-115">-Path가 제공 되지 않으면 스크립트 파일이 현재 디렉터리에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eacd-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6eacd-116">-RecoveryPoint</span></span>
<span data-ttu-id="6eacd-117">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="6eacd-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="6eacd-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6eacd-118">-VaultId</span></span>
<span data-ttu-id="6eacd-119">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6eacd-120">-확인</span><span class="sxs-lookup"><span data-stu-id="6eacd-120">-Confirm</span></span>
<span data-ttu-id="6eacd-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eacd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eacd-122">-WhatIf</span></span>
<span data-ttu-id="6eacd-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eacd-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eacd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eacd-125">CommonParameters</span></span>
<span data-ttu-id="6eacd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eacd-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6eacd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eacd-128">입력</span><span class="sxs-lookup"><span data-stu-id="6eacd-128">INPUTS</span></span>

### <span data-ttu-id="6eacd-129">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="6eacd-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="6eacd-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6eacd-130">System.String</span></span>

## <span data-ttu-id="6eacd-131">출력</span><span class="sxs-lookup"><span data-stu-id="6eacd-131">OUTPUTS</span></span>

### <span data-ttu-id="6eacd-132">RPMountScriptDetails에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="6eacd-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="6eacd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6eacd-133">NOTES</span></span>

## <span data-ttu-id="6eacd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eacd-134">RELATED LINKS</span></span>
