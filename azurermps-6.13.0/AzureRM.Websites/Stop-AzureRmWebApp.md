---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: b389a84ea57902e2e7a7dabaea2d853827a728e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525876"
---
# <span data-ttu-id="0f360-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f360-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="0f360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f360-102">SYNOPSIS</span></span>
<span data-ttu-id="0f360-103">Azure 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f360-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f360-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f360-104">SYNTAX</span></span>

### <span data-ttu-id="0f360-105">S1</span><span class="sxs-lookup"><span data-stu-id="0f360-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f360-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="0f360-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f360-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f360-107">DESCRIPTION</span></span>
<span data-ttu-id="0f360-108">**AzureRmWebApp** Cmdlet은 Azure Web App을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f360-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="0f360-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0f360-109">EXAMPLES</span></span>

### <span data-ttu-id="0f360-110">예제 1: 웹 앱 중지</span><span class="sxs-lookup"><span data-stu-id="0f360-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="0f360-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoWebApp 이라는 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f360-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0f360-112">변수</span><span class="sxs-lookup"><span data-stu-id="0f360-112">PARAMETERS</span></span>

### <span data-ttu-id="0f360-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f360-113">-DefaultProfile</span></span>
<span data-ttu-id="0f360-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f360-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f360-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0f360-115">-Name</span></span>
<span data-ttu-id="0f360-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="0f360-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f360-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f360-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f360-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0f360-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f360-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="0f360-119">-WebApp</span></span>
<span data-ttu-id="0f360-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="0f360-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f360-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f360-121">CommonParameters</span></span>
<span data-ttu-id="0f360-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f360-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f360-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f360-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f360-124">입력</span><span class="sxs-lookup"><span data-stu-id="0f360-124">INPUTS</span></span>

### <span data-ttu-id="0f360-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0f360-125">System.String</span></span>

### <span data-ttu-id="0f360-126">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="0f360-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="0f360-127">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f360-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="0f360-128">출력</span><span class="sxs-lookup"><span data-stu-id="0f360-128">OUTPUTS</span></span>

### <span data-ttu-id="0f360-129">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="0f360-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="0f360-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0f360-130">NOTES</span></span>

## <span data-ttu-id="0f360-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f360-131">RELATED LINKS</span></span>

[<span data-ttu-id="0f360-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f360-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="0f360-133">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f360-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0f360-134">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f360-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0f360-135">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f360-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0f360-136">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f360-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


