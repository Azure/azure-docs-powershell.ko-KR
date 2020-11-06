---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533752"
---
# <span data-ttu-id="8f951-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="8f951-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="8f951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f951-102">SYNOPSIS</span></span>
<span data-ttu-id="8f951-103">서버를 Reregisters 하 여 백업 자격 증명 모음에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f951-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f951-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f951-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f951-105">DESCRIPTION</span></span>
<span data-ttu-id="8f951-106">AzureRmBackupContainerReregistration cmdlet reregisters는 서버를 **사용** 하 여 Azure backup 자격 증명 모음에 연결 하 고 백업 복구 지점을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="8f951-107">서버를 삭제 하면 백업 자격 증명 모음에 모든 클라우드 백업 지점이 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="8f951-108">대체 서버를 만들고 동일한 정규화 된 도메인 이름을 할당 하는 경우 서버를 같은 자격 증명 모음에 다시 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="8f951-109">이 cmdlet을 사용 하면 백업이 백업을 수행 하 고 새 백업 지점을 기존 집합에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="8f951-110">새 서버는 백업 체인에서 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="8f951-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8f951-111">EXAMPLES</span></span>

## <span data-ttu-id="8f951-112">변수</span><span class="sxs-lookup"><span data-stu-id="8f951-112">PARAMETERS</span></span>

### <span data-ttu-id="8f951-113">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="8f951-113">-Container</span></span>
<span data-ttu-id="8f951-114">이 cmdlet이 reregisters 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="8f951-115">**AzureRmBackupContainer** 을 얻으려면 Get-AzureRmBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f951-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f951-116">-DefaultProfile</span></span>
<span data-ttu-id="8f951-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f951-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f951-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f951-118">CommonParameters</span></span>
<span data-ttu-id="8f951-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f951-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f951-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f951-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f951-121">입력</span><span class="sxs-lookup"><span data-stu-id="8f951-121">INPUTS</span></span>

### <span data-ttu-id="8f951-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8f951-122">AzureBackupContainer</span></span>

## <span data-ttu-id="8f951-123">출력</span><span class="sxs-lookup"><span data-stu-id="8f951-123">OUTPUTS</span></span>

### <span data-ttu-id="8f951-124">않아야</span><span class="sxs-lookup"><span data-stu-id="8f951-124">None</span></span>

## <span data-ttu-id="8f951-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8f951-125">NOTES</span></span>

## <span data-ttu-id="8f951-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f951-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f951-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8f951-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="8f951-128">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8f951-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


