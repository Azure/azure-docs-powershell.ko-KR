---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214651"
---
# <span data-ttu-id="2e7e0-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e7e0-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="2e7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7e0-103">Azure 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="2e7e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e7e0-104">SYNTAX</span></span>

### <span data-ttu-id="2e7e0-105">S1</span><span class="sxs-lookup"><span data-stu-id="2e7e0-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e7e0-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2e7e0-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e7e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2e7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="2e7e0-108">**AzWebApp** Cmdlet은 Azure Web App을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="2e7e0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2e7e0-109">EXAMPLES</span></span>

### <span data-ttu-id="2e7e0-110">예제 1: 웹 앱 중지</span><span class="sxs-lookup"><span data-stu-id="2e7e0-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="2e7e0-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoWebApp 이라는 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2e7e0-112">변수</span><span class="sxs-lookup"><span data-stu-id="2e7e0-112">PARAMETERS</span></span>

### <span data-ttu-id="2e7e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7e0-113">-DefaultProfile</span></span>
<span data-ttu-id="2e7e0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e7e0-115">-이름</span><span class="sxs-lookup"><span data-stu-id="2e7e0-115">-Name</span></span>
<span data-ttu-id="2e7e0-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="2e7e0-116">WebApp Name</span></span>

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

### <span data-ttu-id="2e7e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e7e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e7e0-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e7e0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2e7e0-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="2e7e0-119">-WebApp</span></span>
<span data-ttu-id="2e7e0-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="2e7e0-120">WebApp Object</span></span>

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

### <span data-ttu-id="2e7e0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7e0-121">CommonParameters</span></span>
<span data-ttu-id="2e7e0-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7e0-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e7e0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7e0-124">입력</span><span class="sxs-lookup"><span data-stu-id="2e7e0-124">INPUTS</span></span>

### <span data-ttu-id="2e7e0-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e7e0-125">System.String</span></span>

### <span data-ttu-id="2e7e0-126">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2e7e0-127">출력</span><span class="sxs-lookup"><span data-stu-id="2e7e0-127">OUTPUTS</span></span>

### <span data-ttu-id="2e7e0-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="2e7e0-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2e7e0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="2e7e0-129">NOTES</span></span>

## <span data-ttu-id="2e7e0-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e7e0-130">RELATED LINKS</span></span>

[<span data-ttu-id="2e7e0-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e7e0-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="2e7e0-132">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e7e0-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="2e7e0-133">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e7e0-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="2e7e0-134">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e7e0-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="2e7e0-135">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e7e0-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


