---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334094"
---
# <span data-ttu-id="38cd8-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="38cd8-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="38cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38cd8-102">SYNOPSIS</span></span>

<span data-ttu-id="38cd8-103">백업된 항목에 대한 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="38cd8-104">구문</span><span class="sxs-lookup"><span data-stu-id="38cd8-104">SYNTAX</span></span>

### <span data-ttu-id="38cd8-105">NoFilterParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="38cd8-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38cd8-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="38cd8-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38cd8-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="38cd8-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38cd8-108">설명</span><span class="sxs-lookup"><span data-stu-id="38cd8-108">DESCRIPTION</span></span>

<span data-ttu-id="38cd8-109">**Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet은 백업된 Azure Backup 항목에 대한 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="38cd8-110">항목이 백업된 후 **AzureRmRecoveryServicesBackupRecoveryPoint** 개체에는 하나 이상의 복구 지점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="38cd8-111">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="38cd8-112">예제</span><span class="sxs-lookup"><span data-stu-id="38cd8-112">EXAMPLES</span></span>

### <span data-ttu-id="38cd8-113">예제 1: 항목에 대한 지난 주의 복구 지점을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="38cd8-114">첫 번째 명령은 vaultName에 따라 자격 증명 모음 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="38cd8-115">두 번째 명령은 7일 전의 날짜를 인용한 다음, $StartDate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="38cd8-116">세 번째 명령은 오늘 날짜를 인용한 다음, $EndDate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="38cd8-117">네 번째 명령은 AzureVM 백업 컨테이너를 구하고 해당 컨테이너를 $Container 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="38cd8-118">다섯 번째 명령은 workloadType, vaultId에 따라 백업 항목을 10진수에 $BackupItem 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="38cd8-119">마지막 명령은 $BackupItem 항목의 복구 지점 배열을 $RP 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="38cd8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38cd8-120">PARAMETERS</span></span>

### <span data-ttu-id="38cd8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cd8-121">-DefaultProfile</span></span>

<span data-ttu-id="38cd8-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38cd8-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="38cd8-123">-EndDate</span></span>

<span data-ttu-id="38cd8-124">날짜 범위의 끝을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-124">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38cd8-125">-Item</span><span class="sxs-lookup"><span data-stu-id="38cd8-125">-Item</span></span>

<span data-ttu-id="38cd8-126">이 cmdlet이 복구 지점을 얻을 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="38cd8-127">**AzureRmRecoveryServicesBackupItem** 개체를 얻습니다. **Get-AzRecoveryServicesBackupItem** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38cd8-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="38cd8-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="38cd8-129">암호화된 가상 머신에 대한 KeyVault 키를 복원하기 위해 입력 파일을 다운로드할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38cd8-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="38cd8-130">-RecoveryPointId</span></span>

<span data-ttu-id="38cd8-131">복구 지점 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-131">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38cd8-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="38cd8-132">-StartDate</span></span>

<span data-ttu-id="38cd8-133">날짜 범위의 시작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-133">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38cd8-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="38cd8-134">-VaultId</span></span>

<span data-ttu-id="38cd8-135">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="38cd8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cd8-136">CommonParameters</span></span>
<span data-ttu-id="38cd8-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38cd8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cd8-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38cd8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cd8-139">입력</span><span class="sxs-lookup"><span data-stu-id="38cd8-139">INPUTS</span></span>

### <span data-ttu-id="38cd8-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="38cd8-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="38cd8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="38cd8-141">System.String</span></span>

## <span data-ttu-id="38cd8-142">출력</span><span class="sxs-lookup"><span data-stu-id="38cd8-142">OUTPUTS</span></span>

### <span data-ttu-id="38cd8-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="38cd8-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="38cd8-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38cd8-144">NOTES</span></span>

## <span data-ttu-id="38cd8-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38cd8-145">RELATED LINKS</span></span>

[<span data-ttu-id="38cd8-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="38cd8-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="38cd8-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="38cd8-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
