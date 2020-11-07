---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 5b14c694ca61d5c63642012aa954b0e288551b83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698305"
---
# <span data-ttu-id="822a5-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="822a5-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="822a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="822a5-102">SYNOPSIS</span></span>
<span data-ttu-id="822a5-103">Azure Web App을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="822a5-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="822a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="822a5-104">SYNTAX</span></span>

### <span data-ttu-id="822a5-105">S1</span><span class="sxs-lookup"><span data-stu-id="822a5-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="822a5-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="822a5-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="822a5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="822a5-107">DESCRIPTION</span></span>
<span data-ttu-id="822a5-108">**AzWebApp** cmdlet이 중지 된 다음 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="822a5-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="822a5-109">웹 앱이 중지 된 상태 이면 Start-AzWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="822a5-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="822a5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="822a5-110">EXAMPLES</span></span>

### <span data-ttu-id="822a5-111">예제 1: 웹 앱 다시 시작</span><span class="sxs-lookup"><span data-stu-id="822a5-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="822a5-112">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoSite 라는 Azure Web App을 중지 한 다음 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="822a5-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="822a5-113">변수</span><span class="sxs-lookup"><span data-stu-id="822a5-113">PARAMETERS</span></span>

### <span data-ttu-id="822a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822a5-114">-DefaultProfile</span></span>
<span data-ttu-id="822a5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="822a5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822a5-116">-이름</span><span class="sxs-lookup"><span data-stu-id="822a5-116">-Name</span></span>
<span data-ttu-id="822a5-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="822a5-117">WebApp Name</span></span>

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

### <span data-ttu-id="822a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="822a5-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="822a5-119">Resource Group Name</span></span>

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

### <span data-ttu-id="822a5-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="822a5-120">-WebApp</span></span>
<span data-ttu-id="822a5-121">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="822a5-121">WebApp Object</span></span>

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

### <span data-ttu-id="822a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822a5-122">CommonParameters</span></span>
<span data-ttu-id="822a5-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="822a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822a5-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822a5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822a5-125">입력</span><span class="sxs-lookup"><span data-stu-id="822a5-125">INPUTS</span></span>

### <span data-ttu-id="822a5-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="822a5-126">System.String</span></span>

### <span data-ttu-id="822a5-127">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="822a5-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="822a5-128">출력</span><span class="sxs-lookup"><span data-stu-id="822a5-128">OUTPUTS</span></span>

### <span data-ttu-id="822a5-129">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="822a5-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="822a5-130">상속자</span><span class="sxs-lookup"><span data-stu-id="822a5-130">NOTES</span></span>

## <span data-ttu-id="822a5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="822a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="822a5-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="822a5-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="822a5-133">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="822a5-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="822a5-134">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="822a5-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="822a5-135">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="822a5-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="822a5-136">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="822a5-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


