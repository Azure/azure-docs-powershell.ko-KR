---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524207"
---
# <span data-ttu-id="a34f8-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a34f8-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="a34f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a34f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a34f8-103">웹 앱에 사용할 수 있는 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a34f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a34f8-104">SYNTAX</span></span>

### <span data-ttu-id="a34f8-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a34f8-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a34f8-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a34f8-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a34f8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a34f8-107">DESCRIPTION</span></span>
<span data-ttu-id="a34f8-108">**AzureRmWebAppSnapshot** cmdlet은 웹 앱에 대 한 모든 스냅숏을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="a34f8-109">스냅숏은 웹 앱의 파일 및 설정에 대 한 자동 백업입니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="a34f8-110">스냅숏은 **Restore-AzureRmWebAppSnapshot** cmdlet을 사용 하 여 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="a34f8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a34f8-111">EXAMPLES</span></span>

### <span data-ttu-id="a34f8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a34f8-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="a34f8-113">"기본-웹-WestUS" 리소스 그룹에서 "준비" 라는 슬롯을 사용 하 여 "ConstosoApp" 라는 웹 앱에 대 한 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="a34f8-114">변수</span><span class="sxs-lookup"><span data-stu-id="a34f8-114">PARAMETERS</span></span>

### <span data-ttu-id="a34f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34f8-115">-DefaultProfile</span></span>
<span data-ttu-id="a34f8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a34f8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a34f8-117">-Name</span></span>
<span data-ttu-id="a34f8-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a34f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a34f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="a34f8-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a34f8-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="a34f8-121">-Slot</span></span>
<span data-ttu-id="a34f8-122">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a34f8-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="a34f8-123">-WebApp</span></span>
<span data-ttu-id="a34f8-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="a34f8-124">The web app object</span></span>

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

### <span data-ttu-id="a34f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34f8-125">CommonParameters</span></span>
<span data-ttu-id="a34f8-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34f8-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34f8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34f8-128">입력</span><span class="sxs-lookup"><span data-stu-id="a34f8-128">INPUTS</span></span>

### <span data-ttu-id="a34f8-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a34f8-129">System.String</span></span>

### <span data-ttu-id="a34f8-130">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="a34f8-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a34f8-131">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a34f8-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a34f8-132">출력</span><span class="sxs-lookup"><span data-stu-id="a34f8-132">OUTPUTS</span></span>

### <span data-ttu-id="a34f8-133">AzureWebAppSnapshot (\*). i m App.</span><span class="sxs-lookup"><span data-stu-id="a34f8-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="a34f8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a34f8-134">NOTES</span></span>

## <span data-ttu-id="a34f8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a34f8-135">RELATED LINKS</span></span>
