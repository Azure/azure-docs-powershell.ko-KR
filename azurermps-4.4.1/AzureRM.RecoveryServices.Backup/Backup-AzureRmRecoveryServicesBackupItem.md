---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: acf448b58fdf7bcc218ece8b5fb2415bc30981ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703664"
---
# <span data-ttu-id="5e962-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5e962-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5e962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e962-102">SYNOPSIS</span></span>
<span data-ttu-id="5e962-103">백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e962-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e962-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e962-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e962-105">DESCRIPTION</span></span>
<span data-ttu-id="5e962-106">**AzureRmRecoveryServicesBackupItem** cmdlet은 백업 일정에 연결 되지 않은 보호 된 Azure 백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="5e962-107">보호를 사용 하도록 설정 하거나 예약 된 백업이 실패 한 후 백업을 시작 하면 즉시 초기 백업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="5e962-108">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5e962-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5e962-109">EXAMPLES</span></span>

### <span data-ttu-id="5e962-110">예제 1: 백업 항목에 대 한 백업 시작</span><span class="sxs-lookup"><span data-stu-id="5e962-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="5e962-111">첫 번째 명령은 pstestv2vm1 이라는 유형의 Add-azurevm 백업 컨테이너를 가져온 다음이를 $NamedContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="5e962-112">두 번째 명령은 $NamedContainer의 컨테이너에 해당 하는 백업 항목을 가져온 다음 $Item 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="5e962-113">마지막 명령은 $Item에서 백업 항목에 대 한 백업 작업을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="5e962-114">변수</span><span class="sxs-lookup"><span data-stu-id="5e962-114">PARAMETERS</span></span>

### <span data-ttu-id="5e962-115">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="5e962-115">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="5e962-116">만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-116">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="5e962-117">-항목</span><span class="sxs-lookup"><span data-stu-id="5e962-117">-Item</span></span>
<span data-ttu-id="5e962-118">이 cmdlet이 백업 작업을 시작 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-118">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="5e962-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e962-119">-DefaultProfile</span></span>
<span data-ttu-id="5e962-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e962-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e962-121">CommonParameters</span></span>
<span data-ttu-id="5e962-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e962-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e962-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e962-124">입력</span><span class="sxs-lookup"><span data-stu-id="5e962-124">INPUTS</span></span>

### <span data-ttu-id="5e962-125">Dmtf</span><span class="sxs-lookup"><span data-stu-id="5e962-125">DateTime</span></span>
<span data-ttu-id="5e962-126">' ExpiryDateTimeUTC ' 매개 변수는 파이프라인에서 ' DateTime ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-126">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="5e962-127">ItemBase</span><span class="sxs-lookup"><span data-stu-id="5e962-127">ItemBase</span></span>
<span data-ttu-id="5e962-128">' Item ' 매개 변수는 파이프라인에서 ' ItemBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e962-128">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="5e962-129">출력</span><span class="sxs-lookup"><span data-stu-id="5e962-129">OUTPUTS</span></span>

### <span data-ttu-id="5e962-130">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="5e962-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5e962-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5e962-131">NOTES</span></span>

## <span data-ttu-id="5e962-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e962-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e962-133">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5e962-133">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="5e962-134">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5e962-134">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5e962-135">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5e962-135">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


