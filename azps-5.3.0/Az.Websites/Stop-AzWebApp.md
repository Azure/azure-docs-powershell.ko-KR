---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491400"
---
# <span data-ttu-id="392a7-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="392a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="392a7-102">SYNOPSIS</span></span>
<span data-ttu-id="392a7-103">Azure 웹앱을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="392a7-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="392a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="392a7-104">SYNTAX</span></span>

### <span data-ttu-id="392a7-105">S1</span><span class="sxs-lookup"><span data-stu-id="392a7-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="392a7-106">S2</span><span class="sxs-lookup"><span data-stu-id="392a7-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="392a7-107">설명</span><span class="sxs-lookup"><span data-stu-id="392a7-107">DESCRIPTION</span></span>
<span data-ttu-id="392a7-108">**Stop-AzWebApp** cmdlet은 Azure 웹앱을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="392a7-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="392a7-109">예제</span><span class="sxs-lookup"><span data-stu-id="392a7-109">EXAMPLES</span></span>

### <span data-ttu-id="392a7-110">예제 1: 웹앱 중지</span><span class="sxs-lookup"><span data-stu-id="392a7-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="392a7-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoWebApp이라는 웹앱을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="392a7-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="392a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="392a7-112">PARAMETERS</span></span>

### <span data-ttu-id="392a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392a7-113">-DefaultProfile</span></span>
<span data-ttu-id="392a7-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="392a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="392a7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="392a7-115">-Name</span></span>
<span data-ttu-id="392a7-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="392a7-116">WebApp Name</span></span>

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

### <span data-ttu-id="392a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="392a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="392a7-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="392a7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="392a7-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-119">-WebApp</span></span>
<span data-ttu-id="392a7-120">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="392a7-120">WebApp Object</span></span>

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

### <span data-ttu-id="392a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392a7-121">CommonParameters</span></span>
<span data-ttu-id="392a7-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="392a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392a7-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="392a7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392a7-124">입력</span><span class="sxs-lookup"><span data-stu-id="392a7-124">INPUTS</span></span>

### <span data-ttu-id="392a7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="392a7-125">System.String</span></span>

### <span data-ttu-id="392a7-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="392a7-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="392a7-127">출력</span><span class="sxs-lookup"><span data-stu-id="392a7-127">OUTPUTS</span></span>

### <span data-ttu-id="392a7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="392a7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="392a7-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="392a7-129">NOTES</span></span>

## <span data-ttu-id="392a7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="392a7-130">RELATED LINKS</span></span>

[<span data-ttu-id="392a7-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="392a7-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="392a7-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="392a7-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="392a7-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="392a7-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


