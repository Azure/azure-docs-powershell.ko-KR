---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: bfcd198cd629c9b5f1cd37d3d144bc810a6f4b37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526732"
---
# <span data-ttu-id="d8408-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="d8408-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="d8408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8408-102">SYNOPSIS</span></span>
<span data-ttu-id="d8408-103">복구 지점의 모든 파일을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-103">Dismounts all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8408-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8408-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8408-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8408-105">DESCRIPTION</span></span>
<span data-ttu-id="d8408-106">Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet은 Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet을 사용 하 여 이전에 탑재 된 복구 지점의 파일을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-106">The Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="d8408-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8408-107">EXAMPLES</span></span>

### <span data-ttu-id="d8408-108">예제 1: 복구 지점을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-108">Example 1: Dismount a recovery point</span></span>
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

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="d8408-109">변수</span><span class="sxs-lookup"><span data-stu-id="d8408-109">PARAMETERS</span></span>

### <span data-ttu-id="d8408-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8408-110">-DefaultProfile</span></span>
<span data-ttu-id="d8408-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8408-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8408-112">-PassThru</span></span>
<span data-ttu-id="d8408-113">복구 지점을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-113">Return the recovery point.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8408-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d8408-114">-RecoveryPoint</span></span>
<span data-ttu-id="d8408-115">복원할 복구 시점 개체</span><span class="sxs-lookup"><span data-stu-id="d8408-115">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8408-116">-확인</span><span class="sxs-lookup"><span data-stu-id="d8408-116">-Confirm</span></span>
<span data-ttu-id="d8408-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8408-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8408-118">-WhatIf</span></span>
<span data-ttu-id="d8408-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8408-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8408-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8408-121">CommonParameters</span></span>
<span data-ttu-id="d8408-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8408-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8408-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8408-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8408-124">입력</span><span class="sxs-lookup"><span data-stu-id="d8408-124">INPUTS</span></span>

### <span data-ttu-id="d8408-125">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="d8408-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="d8408-126">출력</span><span class="sxs-lookup"><span data-stu-id="d8408-126">OUTPUTS</span></span>

### <span data-ttu-id="d8408-127">System. 개체</span><span class="sxs-lookup"><span data-stu-id="d8408-127">System.Object</span></span>

## <span data-ttu-id="d8408-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d8408-128">NOTES</span></span>

## <span data-ttu-id="d8408-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8408-129">RELATED LINKS</span></span>

