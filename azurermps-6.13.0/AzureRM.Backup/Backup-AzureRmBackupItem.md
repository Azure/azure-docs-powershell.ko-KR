---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534480"
---
# <span data-ttu-id="0c3b4-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0c3b4-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="0c3b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3b4-103">백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c3b4-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c3b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3b4-106">**AzureRmBackupItem** cmdlet은 백업 일정에 연결 되지 않은 보호 된 Azure 백업 항목에 대 한 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="0c3b4-107">보호를 사용 하도록 설정 하거나 예약 된 백업이 실패 한 후 백업을 시작 하면 즉시 초기 백업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="0c3b4-108">기존 백업 작업이 실행 되 고 있는 경우이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="0c3b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c3b4-109">EXAMPLES</span></span>

### <span data-ttu-id="0c3b4-110">예제 1: 가상 컴퓨터 백업 시작</span><span class="sxs-lookup"><span data-stu-id="0c3b4-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="0c3b4-111">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="0c3b4-112">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="0c3b4-113">두 번째 명령은 Get-AzureRmBackupContainer cmdlet을 사용 하 여 $Vault의 자격 증명 모음에서 지정 된 이름을 가진 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="0c3b4-114">명령이 $Container 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="0c3b4-115">마지막 명령은 Get-AzureRmBackupItem cmdlet을 사용 하 여 $Container의 백업 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="0c3b4-116">이 명령은 파이프라인 연산자를 사용 하 여 항목을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0c3b4-117">현재 cmdlet은 컨테이너의 가상 컴퓨터 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="0c3b4-118">변수</span><span class="sxs-lookup"><span data-stu-id="0c3b4-118">PARAMETERS</span></span>

### <span data-ttu-id="0c3b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3b4-119">-DefaultProfile</span></span>
<span data-ttu-id="0c3b4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c3b4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c3b4-121">-항목</span><span class="sxs-lookup"><span data-stu-id="0c3b4-121">-Item</span></span>
<span data-ttu-id="0c3b4-122">이 cmdlet이 백업 작업을 시작 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3b4-123">CommonParameters</span></span>
<span data-ttu-id="0c3b4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3b4-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3b4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3b4-126">입력</span><span class="sxs-lookup"><span data-stu-id="0c3b4-126">INPUTS</span></span>

### <span data-ttu-id="0c3b4-127">AzureRMBackupItem를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="0c3b4-128">매개 변수: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c3b4-128">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="0c3b4-129">출력</span><span class="sxs-lookup"><span data-stu-id="0c3b4-129">OUTPUTS</span></span>

### <span data-ttu-id="0c3b4-130">AzureRMBackupJob를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="0c3b4-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="0c3b4-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0c3b4-131">NOTES</span></span>

## <span data-ttu-id="0c3b4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c3b4-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c3b4-133">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0c3b4-133">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="0c3b4-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0c3b4-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="0c3b4-135">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0c3b4-135">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


