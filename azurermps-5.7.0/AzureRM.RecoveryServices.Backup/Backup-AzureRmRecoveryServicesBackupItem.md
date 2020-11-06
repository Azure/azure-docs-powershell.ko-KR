---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a7451855f62a9e0eab63936107d8431342badfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534743"
---
# <span data-ttu-id="8df01-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8df01-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8df01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df01-102">SYNOPSIS</span></span>
<span data-ttu-id="8df01-103">백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8df01-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df01-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8df01-105">DESCRIPTION</span></span>
<span data-ttu-id="8df01-106">**AzureRmRecoveryServicesBackupItem** cmdlet은 백업 일정에 연결 되지 않은 보호 된 Azure 백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="8df01-107">보호를 사용 하도록 설정 하거나 예약 된 백업이 실패 한 후 백업을 시작 하면 즉시 초기 백업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="8df01-108">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8df01-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8df01-109">EXAMPLES</span></span>

### <span data-ttu-id="8df01-110">예제 1: 백업 항목에 대 한 백업 시작</span><span class="sxs-lookup"><span data-stu-id="8df01-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="8df01-111">첫 번째 명령은 pstestv2vm1 이라는 유형의 Add-azurevm 백업 컨테이너를 가져온 다음이를 $NamedContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="8df01-112">두 번째 명령은 $NamedContainer의 컨테이너에 해당 하는 백업 항목을 가져온 다음 $Item 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="8df01-113">마지막 명령은 $Item에서 백업 항목에 대 한 백업 작업을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="8df01-114">변수</span><span class="sxs-lookup"><span data-stu-id="8df01-114">PARAMETERS</span></span>

### <span data-ttu-id="8df01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df01-115">-DefaultProfile</span></span>
<span data-ttu-id="8df01-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8df01-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="8df01-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="8df01-118">만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df01-119">-항목</span><span class="sxs-lookup"><span data-stu-id="8df01-119">-Item</span></span>
<span data-ttu-id="8df01-120">이 cmdlet이 백업 작업을 시작 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df01-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8df01-121">-Confirm</span></span>
<span data-ttu-id="8df01-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df01-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df01-123">-WhatIf</span></span>
<span data-ttu-id="8df01-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8df01-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df01-126">CommonParameters</span></span>
<span data-ttu-id="8df01-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df01-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df01-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df01-129">입력</span><span class="sxs-lookup"><span data-stu-id="8df01-129">INPUTS</span></span>

### <span data-ttu-id="8df01-130">Dmtf</span><span class="sxs-lookup"><span data-stu-id="8df01-130">DateTime</span></span>
<span data-ttu-id="8df01-131">' ExpiryDateTimeUTC ' 매개 변수는 파이프라인에서 ' DateTime ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-131">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="8df01-132">ItemBase</span><span class="sxs-lookup"><span data-stu-id="8df01-132">ItemBase</span></span>
<span data-ttu-id="8df01-133">' Item ' 매개 변수는 파이프라인에서 ' ItemBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df01-133">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="8df01-134">출력</span><span class="sxs-lookup"><span data-stu-id="8df01-134">OUTPUTS</span></span>

### <span data-ttu-id="8df01-135">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="8df01-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8df01-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8df01-136">NOTES</span></span>

## <span data-ttu-id="8df01-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8df01-137">RELATED LINKS</span></span>

[<span data-ttu-id="8df01-138">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8df01-138">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="8df01-139">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8df01-139">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="8df01-140">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8df01-140">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


