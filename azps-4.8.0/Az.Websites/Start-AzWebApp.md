---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212008"
---
# <span data-ttu-id="6f591-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f591-101">Start-AzWebApp</span></span>

## <span data-ttu-id="6f591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f591-102">SYNOPSIS</span></span>
<span data-ttu-id="6f591-103">Azure 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f591-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="6f591-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f591-104">SYNTAX</span></span>

### <span data-ttu-id="6f591-105">S1</span><span class="sxs-lookup"><span data-stu-id="6f591-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f591-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="6f591-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f591-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f591-107">DESCRIPTION</span></span>
<span data-ttu-id="6f591-108">**AzWebApp** Cmdlet은 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f591-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="6f591-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6f591-109">EXAMPLES</span></span>

### <span data-ttu-id="6f591-110">예제 1: 웹 앱 시작</span><span class="sxs-lookup"><span data-stu-id="6f591-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="6f591-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f591-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6f591-112">변수</span><span class="sxs-lookup"><span data-stu-id="6f591-112">PARAMETERS</span></span>

### <span data-ttu-id="6f591-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f591-113">-DefaultProfile</span></span>
<span data-ttu-id="6f591-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f591-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f591-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6f591-115">-Name</span></span>
<span data-ttu-id="6f591-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="6f591-116">WebApp Name</span></span>

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

### <span data-ttu-id="6f591-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f591-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f591-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6f591-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6f591-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="6f591-119">-WebApp</span></span>
<span data-ttu-id="6f591-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="6f591-120">WebApp Object</span></span>

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

### <span data-ttu-id="6f591-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f591-121">CommonParameters</span></span>
<span data-ttu-id="6f591-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f591-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f591-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f591-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f591-124">입력</span><span class="sxs-lookup"><span data-stu-id="6f591-124">INPUTS</span></span>

### <span data-ttu-id="6f591-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f591-125">System.String</span></span>

### <span data-ttu-id="6f591-126">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="6f591-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6f591-127">출력</span><span class="sxs-lookup"><span data-stu-id="6f591-127">OUTPUTS</span></span>

### <span data-ttu-id="6f591-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="6f591-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6f591-129">상속자</span><span class="sxs-lookup"><span data-stu-id="6f591-129">NOTES</span></span>

## <span data-ttu-id="6f591-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f591-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f591-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f591-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="6f591-132">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f591-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="6f591-133">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f591-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="6f591-134">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f591-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="6f591-135">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f591-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


