---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8223172994eb4fdbea3c887f788c4b0e445e0202
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526699"
---
# <span data-ttu-id="f24a7-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f24a7-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="f24a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f24a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f24a7-103">백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f24a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f24a7-104">SYNTAX</span></span>

### <span data-ttu-id="f24a7-105">NoFilterParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f24a7-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f24a7-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f24a7-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f24a7-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f24a7-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f24a7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f24a7-108">DESCRIPTION</span></span>
<span data-ttu-id="f24a7-109">**AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet은 백업 된 Azure 백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f24a7-110">항목을 백업한 후 **AzureRmRecoveryServicesBackupRecoveryPoint** 개체에는 하나 이상의 복구 지점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="f24a7-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f24a7-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f24a7-112">EXAMPLES</span></span>

### <span data-ttu-id="f24a7-113">예제 1: 항목에 대 한 지난 주의 복구 지점 가져오기</span><span class="sxs-lookup"><span data-stu-id="f24a7-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="f24a7-114">첫 번째 명령은 7 일 전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="f24a7-115">두 번째 명령은 오늘 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="f24a7-116">세 번째 명령은 Add-azurevm 백업 컨테이너를 가져와 $Containers 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="f24a7-117">네 번째 명령은 V2VM 이라는 백업 항목을 가져온 다음이를 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="f24a7-118">마지막 명령은 $BackupItem의 항목에 대 한 복구 지점 배열을 가져온 다음 $RP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f24a7-119">변수</span><span class="sxs-lookup"><span data-stu-id="f24a7-119">PARAMETERS</span></span>

### <span data-ttu-id="f24a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24a7-120">-DefaultProfile</span></span>
<span data-ttu-id="f24a7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f24a7-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f24a7-122">-EndDate</span></span>
<span data-ttu-id="f24a7-123">날짜 범위의 끝을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-123">Specifies the end of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24a7-124">-항목</span><span class="sxs-lookup"><span data-stu-id="f24a7-124">-Item</span></span>
<span data-ttu-id="f24a7-125">이 cmdlet이 복구 지점을 가져오는 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f24a7-126">**AzureRmRecoveryServicesBackupItem** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f24a7-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="f24a7-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="f24a7-128">암호화 된 가상 컴퓨터에 대 한 KeyVault 키를 복원 하기 위해 입력 파일을 다운로드할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24a7-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f24a7-129">-RecoveryPointId</span></span>
<span data-ttu-id="f24a7-130">복구 지점의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-130">Specifies the recovery point ID.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24a7-131">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="f24a7-131">-StartDate</span></span>
<span data-ttu-id="f24a7-132">날짜 범위의 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-132">Specifies the start of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24a7-133">CommonParameters</span></span>
<span data-ttu-id="f24a7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24a7-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f24a7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24a7-136">입력</span><span class="sxs-lookup"><span data-stu-id="f24a7-136">INPUTS</span></span>

### <span data-ttu-id="f24a7-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="f24a7-137">ItemBase</span></span>
<span data-ttu-id="f24a7-138">' Item ' 매개 변수는 파이프라인에서 ' ItemBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f24a7-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="f24a7-139">출력</span><span class="sxs-lookup"><span data-stu-id="f24a7-139">OUTPUTS</span></span>

### <span data-ttu-id="f24a7-140">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="f24a7-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="f24a7-141">System.webserver. IList ' 1 [Microsoft Azure. e. RecoveryPointBase]을 (를)</span><span class="sxs-lookup"><span data-stu-id="f24a7-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="f24a7-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f24a7-142">NOTES</span></span>

## <span data-ttu-id="f24a7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f24a7-143">RELATED LINKS</span></span>

[<span data-ttu-id="f24a7-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f24a7-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f24a7-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f24a7-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


