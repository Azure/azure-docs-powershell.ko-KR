---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876098"
---
# <span data-ttu-id="a6a11-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6a11-101">Start-AzWebApp</span></span>

## <span data-ttu-id="a6a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a11-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a11-103">Azure 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a11-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="a6a11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6a11-104">SYNTAX</span></span>

### <span data-ttu-id="a6a11-105">S1</span><span class="sxs-lookup"><span data-stu-id="a6a11-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6a11-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="a6a11-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a11-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a6a11-107">DESCRIPTION</span></span>
<span data-ttu-id="a6a11-108">**AzWebApp** Cmdlet은 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a11-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="a6a11-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a6a11-109">EXAMPLES</span></span>

### <span data-ttu-id="a6a11-110">예제 1: 웹 앱 시작</span><span class="sxs-lookup"><span data-stu-id="a6a11-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a6a11-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a11-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a6a11-112">변수</span><span class="sxs-lookup"><span data-stu-id="a6a11-112">PARAMETERS</span></span>

### <span data-ttu-id="a6a11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a11-113">-DefaultProfile</span></span>
<span data-ttu-id="a6a11-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a11-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a11-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a6a11-115">-Name</span></span>
<span data-ttu-id="a6a11-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="a6a11-116">WebApp Name</span></span>

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

### <span data-ttu-id="a6a11-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a11-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6a11-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a6a11-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a6a11-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="a6a11-119">-WebApp</span></span>
<span data-ttu-id="a6a11-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="a6a11-120">WebApp Object</span></span>

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

### <span data-ttu-id="a6a11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a11-121">CommonParameters</span></span>
<span data-ttu-id="a6a11-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a11-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a11-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a11-124">입력</span><span class="sxs-lookup"><span data-stu-id="a6a11-124">INPUTS</span></span>

### <span data-ttu-id="a6a11-125">Site</span><span class="sxs-lookup"><span data-stu-id="a6a11-125">Site</span></span>
<span data-ttu-id="a6a11-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a11-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a6a11-127">출력</span><span class="sxs-lookup"><span data-stu-id="a6a11-127">OUTPUTS</span></span>

## <span data-ttu-id="a6a11-128">상속자</span><span class="sxs-lookup"><span data-stu-id="a6a11-128">NOTES</span></span>

## <span data-ttu-id="a6a11-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a11-129">RELATED LINKS</span></span>

[<span data-ttu-id="a6a11-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6a11-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a6a11-131">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6a11-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a6a11-132">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6a11-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a6a11-133">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6a11-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a6a11-134">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6a11-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


