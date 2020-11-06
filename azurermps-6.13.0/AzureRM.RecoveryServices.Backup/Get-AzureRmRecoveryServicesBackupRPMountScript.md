---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6caf37bf8e9b4bc11969ff4f1e0e55e7e0d6880c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531339"
---
# <span data-ttu-id="50d56-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="50d56-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="50d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d56-102">SYNOPSIS</span></span>
<span data-ttu-id="50d56-103">복구 지점의 모든 파일을 탑재 하는 스크립트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50d56-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50d56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50d56-105">DESCRIPTION</span></span>
<span data-ttu-id="50d56-106">Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet은 앱이 실행 되는 컴퓨터에 복구 지점의 볼륨을 탑재 하는 스크립트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="50d56-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50d56-107">EXAMPLES</span></span>

### <span data-ttu-id="50d56-108">예제 1: 복구 지점을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="50d56-109">스크립트를 실행 하면 복구 지점의 파일이 $rp 0이 탑재 됩니다. \[\]</span><span class="sxs-lookup"><span data-stu-id="50d56-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="50d56-110">변수</span><span class="sxs-lookup"><span data-stu-id="50d56-110">PARAMETERS</span></span>

### <span data-ttu-id="50d56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d56-111">-DefaultProfile</span></span>
<span data-ttu-id="50d56-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d56-113">-Path</span><span class="sxs-lookup"><span data-stu-id="50d56-113">-Path</span></span>
<span data-ttu-id="50d56-114">파일을 복구 하는 경우 파일을 다운로드할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="50d56-115">-Path가 제공 되지 않으면 스크립트 파일이 현재 디렉터리에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

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

### <span data-ttu-id="50d56-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="50d56-116">-RecoveryPoint</span></span>
<span data-ttu-id="50d56-117">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="50d56-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="50d56-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="50d56-118">-VaultId</span></span>
<span data-ttu-id="50d56-119">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="50d56-120">-확인</span><span class="sxs-lookup"><span data-stu-id="50d56-120">-Confirm</span></span>
<span data-ttu-id="50d56-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50d56-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d56-122">-WhatIf</span></span>
<span data-ttu-id="50d56-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d56-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50d56-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d56-125">CommonParameters</span></span>
<span data-ttu-id="50d56-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d56-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d56-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d56-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d56-128">입력</span><span class="sxs-lookup"><span data-stu-id="50d56-128">INPUTS</span></span>

### <span data-ttu-id="50d56-129">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="50d56-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="50d56-130">매개 변수: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50d56-130">Parameters: RecoveryPoint (ByValue)</span></span>

### <span data-ttu-id="50d56-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50d56-131">System.String</span></span>
<span data-ttu-id="50d56-132">매개 변수: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50d56-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="50d56-133">출력</span><span class="sxs-lookup"><span data-stu-id="50d56-133">OUTPUTS</span></span>

### <span data-ttu-id="50d56-134">RPMountScriptDetails에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="50d56-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="50d56-135">상속자</span><span class="sxs-lookup"><span data-stu-id="50d56-135">NOTES</span></span>

## <span data-ttu-id="50d56-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50d56-136">RELATED LINKS</span></span>
