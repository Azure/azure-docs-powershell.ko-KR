---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: 98ded2967c364955ab8b9dd38f316021649d0fc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529313"
---
# <span data-ttu-id="9a743-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="9a743-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="9a743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a743-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a743-103">구문과</span><span class="sxs-lookup"><span data-stu-id="9a743-103">SYNTAX</span></span>

### <span data-ttu-id="9a743-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9a743-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a743-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9a743-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a743-106">설명은</span><span class="sxs-lookup"><span data-stu-id="9a743-106">DESCRIPTION</span></span>
<span data-ttu-id="9a743-107">**AzureRmWebAppBackup** cmdlet은 지정 된 Azure Web App 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a743-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="9a743-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9a743-108">EXAMPLES</span></span>

### <span data-ttu-id="9a743-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="9a743-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="9a743-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 ID가 "12345" 인 백업을 사용 하 여 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a743-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9a743-111">변수</span><span class="sxs-lookup"><span data-stu-id="9a743-111">PARAMETERS</span></span>

### <span data-ttu-id="9a743-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="9a743-112">-BackupId</span></span>
<span data-ttu-id="9a743-113">백업 Id</span><span class="sxs-lookup"><span data-stu-id="9a743-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a743-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a743-114">-DefaultProfile</span></span>
<span data-ttu-id="9a743-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a743-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a743-116">-이름</span><span class="sxs-lookup"><span data-stu-id="9a743-116">-Name</span></span>
<span data-ttu-id="9a743-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9a743-117">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a743-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a743-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a743-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a743-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a743-120">-슬롯</span><span class="sxs-lookup"><span data-stu-id="9a743-120">-Slot</span></span>
<span data-ttu-id="9a743-121">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="9a743-121">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a743-122">-Web app</span><span class="sxs-lookup"><span data-stu-id="9a743-122">-WebApp</span></span>
<span data-ttu-id="9a743-123">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="9a743-123">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a743-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a743-124">CommonParameters</span></span>
<span data-ttu-id="9a743-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a743-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a743-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a743-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a743-127">입력</span><span class="sxs-lookup"><span data-stu-id="9a743-127">INPUTS</span></span>

### <span data-ttu-id="9a743-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a743-128">System.String</span></span>

### <span data-ttu-id="9a743-129">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="9a743-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="9a743-130">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a743-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="9a743-131">출력</span><span class="sxs-lookup"><span data-stu-id="9a743-131">OUTPUTS</span></span>

### <span data-ttu-id="9a743-132">Microsoft. Azure. 관리자.</span><span class="sxs-lookup"><span data-stu-id="9a743-132">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="9a743-133">상속자</span><span class="sxs-lookup"><span data-stu-id="9a743-133">NOTES</span></span>

## <span data-ttu-id="9a743-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a743-134">RELATED LINKS</span></span>
