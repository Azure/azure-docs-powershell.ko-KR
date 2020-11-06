---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 20acba9bc0f08857c9bdfaaf559544f26b4902ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525443"
---
# <span data-ttu-id="2a10a-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a10a-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="2a10a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a10a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a10a-103">Azure 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10a-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a10a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a10a-104">SYNTAX</span></span>

### <span data-ttu-id="2a10a-105">S1</span><span class="sxs-lookup"><span data-stu-id="2a10a-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a10a-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2a10a-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a10a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2a10a-107">DESCRIPTION</span></span>
<span data-ttu-id="2a10a-108">**AzureRmWebApp** Cmdlet은 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10a-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="2a10a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2a10a-109">EXAMPLES</span></span>

### <span data-ttu-id="2a10a-110">예제 1: 웹 앱 시작</span><span class="sxs-lookup"><span data-stu-id="2a10a-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="2a10a-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10a-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2a10a-112">변수</span><span class="sxs-lookup"><span data-stu-id="2a10a-112">PARAMETERS</span></span>

### <span data-ttu-id="2a10a-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2a10a-113">-Name</span></span>
<span data-ttu-id="2a10a-114">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="2a10a-114">WebApp Name</span></span>

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

### <span data-ttu-id="2a10a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a10a-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a10a-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2a10a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2a10a-117">-Web app</span><span class="sxs-lookup"><span data-stu-id="2a10a-117">-WebApp</span></span>
<span data-ttu-id="2a10a-118">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="2a10a-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a10a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a10a-119">-DefaultProfile</span></span>
<span data-ttu-id="2a10a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a10a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a10a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a10a-121">CommonParameters</span></span>
<span data-ttu-id="2a10a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a10a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a10a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a10a-124">입력</span><span class="sxs-lookup"><span data-stu-id="2a10a-124">INPUTS</span></span>

### <span data-ttu-id="2a10a-125">Site</span><span class="sxs-lookup"><span data-stu-id="2a10a-125">Site</span></span>
<span data-ttu-id="2a10a-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10a-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2a10a-127">출력</span><span class="sxs-lookup"><span data-stu-id="2a10a-127">OUTPUTS</span></span>

## <span data-ttu-id="2a10a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="2a10a-128">NOTES</span></span>

## <span data-ttu-id="2a10a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a10a-129">RELATED LINKS</span></span>

[<span data-ttu-id="2a10a-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a10a-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2a10a-131">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a10a-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2a10a-132">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a10a-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2a10a-133">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a10a-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2a10a-134">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a10a-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


