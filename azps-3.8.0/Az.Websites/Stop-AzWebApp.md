---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042585"
---
# <span data-ttu-id="3e6ae-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e6ae-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="3e6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6ae-103">Azure 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="3e6ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e6ae-104">SYNTAX</span></span>

### <span data-ttu-id="3e6ae-105">S1</span><span class="sxs-lookup"><span data-stu-id="3e6ae-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e6ae-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="3e6ae-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6ae-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3e6ae-107">DESCRIPTION</span></span>
<span data-ttu-id="3e6ae-108">**AzWebApp** Cmdlet은 Azure Web App을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="3e6ae-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3e6ae-109">EXAMPLES</span></span>

### <span data-ttu-id="3e6ae-110">예제 1: 웹 앱 중지</span><span class="sxs-lookup"><span data-stu-id="3e6ae-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="3e6ae-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoWebApp 이라는 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3e6ae-112">변수</span><span class="sxs-lookup"><span data-stu-id="3e6ae-112">PARAMETERS</span></span>

### <span data-ttu-id="3e6ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6ae-113">-DefaultProfile</span></span>
<span data-ttu-id="3e6ae-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e6ae-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3e6ae-115">-Name</span></span>
<span data-ttu-id="3e6ae-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="3e6ae-116">WebApp Name</span></span>

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

### <span data-ttu-id="3e6ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e6ae-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3e6ae-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3e6ae-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="3e6ae-119">-WebApp</span></span>
<span data-ttu-id="3e6ae-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="3e6ae-120">WebApp Object</span></span>

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

### <span data-ttu-id="3e6ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6ae-121">CommonParameters</span></span>
<span data-ttu-id="3e6ae-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6ae-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6ae-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6ae-124">입력</span><span class="sxs-lookup"><span data-stu-id="3e6ae-124">INPUTS</span></span>

### <span data-ttu-id="3e6ae-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3e6ae-125">System.String</span></span>

### <span data-ttu-id="3e6ae-126">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3e6ae-127">출력</span><span class="sxs-lookup"><span data-stu-id="3e6ae-127">OUTPUTS</span></span>

### <span data-ttu-id="3e6ae-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3e6ae-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3e6ae-129">NOTES</span></span>

## <span data-ttu-id="3e6ae-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e6ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e6ae-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e6ae-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3e6ae-132">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e6ae-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3e6ae-133">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e6ae-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3e6ae-134">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e6ae-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3e6ae-135">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e6ae-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


