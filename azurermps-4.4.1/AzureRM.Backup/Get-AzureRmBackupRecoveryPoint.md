---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528288"
---
# <span data-ttu-id="17240-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="17240-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="17240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17240-102">SYNOPSIS</span></span>
<span data-ttu-id="17240-103">백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17240-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17240-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17240-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17240-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17240-105">DESCRIPTION</span></span>
<span data-ttu-id="17240-106">**AzureRmBackupRecoveryPoint** cmdlet은 백업 된 Azure 백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17240-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="17240-107">항목을 백업한 후에는 백업이 하나 이상의 복구 지점을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="17240-108">예제의</span><span class="sxs-lookup"><span data-stu-id="17240-108">EXAMPLES</span></span>

### <span data-ttu-id="17240-109">예제 1: 항목에 대 한 복구 지점 가져오기</span><span class="sxs-lookup"><span data-stu-id="17240-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="17240-110">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17240-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="17240-111">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="17240-112">두 번째 명령은 **AzureRmBackupContainer** cmdlet을 사용 하 여 $Vault의 자격 증명 모음에서 지정 된 이름을 가진 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17240-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="17240-113">명령이 $Container 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="17240-114">세 번째 명령은 **AzureRmBackupItem** cmdlet을 사용 하 여 $Container의 컨테이너에 있는 백업 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17240-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="17240-115">명령이 $BackupItem 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="17240-116">마지막 명령은 $BackupItem 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17240-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="17240-117">변수</span><span class="sxs-lookup"><span data-stu-id="17240-117">PARAMETERS</span></span>

### <span data-ttu-id="17240-118">-항목</span><span class="sxs-lookup"><span data-stu-id="17240-118">-Item</span></span>
<span data-ttu-id="17240-119">이 cmdlet이 복구 지점을 가져오는 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-119">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="17240-120">**AzureRmBackupItem** 을 얻으려면 Get-AzureRmBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-120">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="17240-121">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="17240-121">-RecoveryPointId</span></span>
<span data-ttu-id="17240-122">이 cmdlet이 가져오는 복구 지점의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-122">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="17240-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17240-123">-DefaultProfile</span></span>
<span data-ttu-id="17240-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17240-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17240-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17240-125">CommonParameters</span></span>
<span data-ttu-id="17240-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17240-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17240-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17240-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17240-128">입력</span><span class="sxs-lookup"><span data-stu-id="17240-128">INPUTS</span></span>

### <span data-ttu-id="17240-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="17240-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="17240-130">출력</span><span class="sxs-lookup"><span data-stu-id="17240-130">OUTPUTS</span></span>

### <span data-ttu-id="17240-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="17240-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="17240-132">상속자</span><span class="sxs-lookup"><span data-stu-id="17240-132">NOTES</span></span>

## <span data-ttu-id="17240-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17240-133">RELATED LINKS</span></span>

[<span data-ttu-id="17240-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="17240-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="17240-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="17240-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="17240-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="17240-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


