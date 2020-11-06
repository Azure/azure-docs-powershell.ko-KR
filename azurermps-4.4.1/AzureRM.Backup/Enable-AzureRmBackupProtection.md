---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527720"
---
# <span data-ttu-id="8096f-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8096f-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="8096f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8096f-102">SYNOPSIS</span></span>
<span data-ttu-id="8096f-103">항목을 Azure 백업 보호 정책에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8096f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8096f-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8096f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8096f-105">DESCRIPTION</span></span>
<span data-ttu-id="8096f-106">**AzureRmBackupProtection** cmdlet은 항목을 Azure 백업 보호 정책과 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="8096f-107">보호 정책을 사용 하도록 설정 하려면 먼저 기존 백업 항목과 기존 정책이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="8096f-108">두 가지 모두 동일한 백업 자격 증명 모음에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="8096f-109">백업 일정은 항목에 대 한 전체 초기 복사본을, 이후 백업의 증분 복사본을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="8096f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8096f-110">EXAMPLES</span></span>

### <span data-ttu-id="8096f-111">예제 1: Azure 가상 컴퓨터에서 보호 사용</span><span class="sxs-lookup"><span data-stu-id="8096f-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="8096f-112">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="8096f-113">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="8096f-114">두 번째 명령은 $Vault의 자격 증명 모음에 대 한 DefaultPolicy 라는 백업 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="8096f-115">명령이 $Policy 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="8096f-116">마지막 명령은 파이프라인 연산자를 사용 하 여 한 cmdlet의 값을 다음으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="8096f-117">이 메서드는 Get-AzureRmBackupContainer cmdlet을 사용 하 여 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="8096f-118">이 명령은 Get-AzureRmBackupItem cmdlet을 사용 하 여 해당 컨테이너에서 백업 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="8096f-119">현재 cmdlet은 명령이 해당 cmdlet에 전달 하는 항목에 대 한 $Policy에 저장 된 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="8096f-120">변수</span><span class="sxs-lookup"><span data-stu-id="8096f-120">PARAMETERS</span></span>

### <span data-ttu-id="8096f-121">-항목</span><span class="sxs-lookup"><span data-stu-id="8096f-121">-Item</span></span>
<span data-ttu-id="8096f-122">이 cmdlet이 보호할 수 있는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="8096f-123">**AzureRmBackupItem** 을 얻으려면 Get-AzureRmBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8096f-124">-정책</span><span class="sxs-lookup"><span data-stu-id="8096f-124">-Policy</span></span>
<span data-ttu-id="8096f-125">이 cmdlet이 항목과 연결 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="8096f-126">**AzureRmBackupProtectionPolicy** 개체를 가져오려면 Get-AzureRmBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8096f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8096f-127">-DefaultProfile</span></span>
<span data-ttu-id="8096f-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8096f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8096f-129">CommonParameters</span></span>
<span data-ttu-id="8096f-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8096f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8096f-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8096f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8096f-132">입력</span><span class="sxs-lookup"><span data-stu-id="8096f-132">INPUTS</span></span>

### <span data-ttu-id="8096f-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="8096f-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="8096f-134">출력</span><span class="sxs-lookup"><span data-stu-id="8096f-134">OUTPUTS</span></span>

### <span data-ttu-id="8096f-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8096f-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="8096f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8096f-136">NOTES</span></span>

## <span data-ttu-id="8096f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8096f-137">RELATED LINKS</span></span>

[<span data-ttu-id="8096f-138">백업-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="8096f-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="8096f-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="8096f-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="8096f-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8096f-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


