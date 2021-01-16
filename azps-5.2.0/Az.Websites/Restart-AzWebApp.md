---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326045"
---
# <span data-ttu-id="ec662-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="ec662-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec662-102">SYNOPSIS</span></span>
<span data-ttu-id="ec662-103">Azure 웹앱을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ec662-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="ec662-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec662-104">SYNTAX</span></span>

### <span data-ttu-id="ec662-105">S1</span><span class="sxs-lookup"><span data-stu-id="ec662-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec662-106">S2</span><span class="sxs-lookup"><span data-stu-id="ec662-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec662-107">설명</span><span class="sxs-lookup"><span data-stu-id="ec662-107">DESCRIPTION</span></span>
<span data-ttu-id="ec662-108">**Restart-AzWebApp** cmdlet이 중지된 다음 Azure 웹앱을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ec662-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="ec662-109">웹앱이 중지된 상태인 경우 Start-AzWebApp cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="ec662-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="ec662-110">예제</span><span class="sxs-lookup"><span data-stu-id="ec662-110">EXAMPLES</span></span>

### <span data-ttu-id="ec662-111">예제 1: 웹앱 다시 시작</span><span class="sxs-lookup"><span data-stu-id="ec662-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ec662-112">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure 웹앱을 중지한 다음 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ec662-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="ec662-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec662-113">PARAMETERS</span></span>

### <span data-ttu-id="ec662-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec662-114">-DefaultProfile</span></span>
<span data-ttu-id="ec662-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec662-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec662-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ec662-116">-Name</span></span>
<span data-ttu-id="ec662-117">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="ec662-117">WebApp Name</span></span>

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

### <span data-ttu-id="ec662-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec662-118">-ResourceGroupName</span></span>
<span data-ttu-id="ec662-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ec662-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ec662-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-120">-WebApp</span></span>
<span data-ttu-id="ec662-121">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="ec662-121">WebApp Object</span></span>

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

### <span data-ttu-id="ec662-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec662-122">CommonParameters</span></span>
<span data-ttu-id="ec662-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec662-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec662-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec662-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec662-125">입력</span><span class="sxs-lookup"><span data-stu-id="ec662-125">INPUTS</span></span>

### <span data-ttu-id="ec662-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ec662-126">System.String</span></span>

### <span data-ttu-id="ec662-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ec662-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec662-128">출력</span><span class="sxs-lookup"><span data-stu-id="ec662-128">OUTPUTS</span></span>

### <span data-ttu-id="ec662-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ec662-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec662-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec662-130">NOTES</span></span>

## <span data-ttu-id="ec662-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec662-131">RELATED LINKS</span></span>

[<span data-ttu-id="ec662-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ec662-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ec662-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ec662-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ec662-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec662-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

