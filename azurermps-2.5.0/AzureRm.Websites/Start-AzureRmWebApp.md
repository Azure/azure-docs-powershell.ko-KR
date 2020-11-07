---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: b05ba189c4b718689f95acac1bfcead84cd3415b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882097"
---
# <span data-ttu-id="1a8d3-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1a8d3-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="1a8d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8d3-103">Azure 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a8d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a8d3-104">SYNTAX</span></span>

### <span data-ttu-id="1a8d3-105">S1</span><span class="sxs-lookup"><span data-stu-id="1a8d3-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a8d3-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="1a8d3-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a8d3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1a8d3-107">DESCRIPTION</span></span>
<span data-ttu-id="1a8d3-108">**AzureRmWebApp** Cmdlet은 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="1a8d3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1a8d3-109">EXAMPLES</span></span>

### <span data-ttu-id="1a8d3-110">예제 1: 웹 앱 시작</span><span class="sxs-lookup"><span data-stu-id="1a8d3-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="1a8d3-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1a8d3-112">변수</span><span class="sxs-lookup"><span data-stu-id="1a8d3-112">PARAMETERS</span></span>

### <span data-ttu-id="1a8d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8d3-113">-DefaultProfile</span></span>
<span data-ttu-id="1a8d3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a8d3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1a8d3-115">-Name</span></span>
<span data-ttu-id="1a8d3-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="1a8d3-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a8d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a8d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a8d3-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1a8d3-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8d3-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="1a8d3-119">-WebApp</span></span>
<span data-ttu-id="1a8d3-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="1a8d3-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a8d3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8d3-121">CommonParameters</span></span>
<span data-ttu-id="1a8d3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8d3-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8d3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8d3-124">입력</span><span class="sxs-lookup"><span data-stu-id="1a8d3-124">INPUTS</span></span>

### <span data-ttu-id="1a8d3-125">Site</span><span class="sxs-lookup"><span data-stu-id="1a8d3-125">Site</span></span>
<span data-ttu-id="1a8d3-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1a8d3-127">출력</span><span class="sxs-lookup"><span data-stu-id="1a8d3-127">OUTPUTS</span></span>

## <span data-ttu-id="1a8d3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="1a8d3-128">NOTES</span></span>

## <span data-ttu-id="1a8d3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a8d3-129">RELATED LINKS</span></span>

[<span data-ttu-id="1a8d3-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1a8d3-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1a8d3-131">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1a8d3-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1a8d3-132">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1a8d3-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1a8d3-133">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1a8d3-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1a8d3-134">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1a8d3-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


