---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876084"
---
# <span data-ttu-id="75eed-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="75eed-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="75eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75eed-102">SYNOPSIS</span></span>
<span data-ttu-id="75eed-103">Azure 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75eed-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="75eed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75eed-104">SYNTAX</span></span>

### <span data-ttu-id="75eed-105">S1</span><span class="sxs-lookup"><span data-stu-id="75eed-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75eed-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="75eed-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75eed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="75eed-107">DESCRIPTION</span></span>
<span data-ttu-id="75eed-108">**AzWebApp** Cmdlet은 Azure Web App을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75eed-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="75eed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="75eed-109">EXAMPLES</span></span>

### <span data-ttu-id="75eed-110">예제 1: 웹 앱 중지</span><span class="sxs-lookup"><span data-stu-id="75eed-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="75eed-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoWebApp 이라는 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75eed-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="75eed-112">변수</span><span class="sxs-lookup"><span data-stu-id="75eed-112">PARAMETERS</span></span>

### <span data-ttu-id="75eed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75eed-113">-DefaultProfile</span></span>
<span data-ttu-id="75eed-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75eed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75eed-115">-이름</span><span class="sxs-lookup"><span data-stu-id="75eed-115">-Name</span></span>
<span data-ttu-id="75eed-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="75eed-116">WebApp Name</span></span>

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

### <span data-ttu-id="75eed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75eed-117">-ResourceGroupName</span></span>
<span data-ttu-id="75eed-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="75eed-118">Resource Group Name</span></span>

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

### <span data-ttu-id="75eed-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="75eed-119">-WebApp</span></span>
<span data-ttu-id="75eed-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="75eed-120">WebApp Object</span></span>

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

### <span data-ttu-id="75eed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75eed-121">CommonParameters</span></span>
<span data-ttu-id="75eed-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75eed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75eed-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75eed-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75eed-124">입력</span><span class="sxs-lookup"><span data-stu-id="75eed-124">INPUTS</span></span>

### <span data-ttu-id="75eed-125">Site</span><span class="sxs-lookup"><span data-stu-id="75eed-125">Site</span></span>
<span data-ttu-id="75eed-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75eed-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="75eed-127">출력</span><span class="sxs-lookup"><span data-stu-id="75eed-127">OUTPUTS</span></span>

## <span data-ttu-id="75eed-128">상속자</span><span class="sxs-lookup"><span data-stu-id="75eed-128">NOTES</span></span>

## <span data-ttu-id="75eed-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75eed-129">RELATED LINKS</span></span>

[<span data-ttu-id="75eed-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="75eed-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="75eed-131">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="75eed-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="75eed-132">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="75eed-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="75eed-133">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="75eed-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="75eed-134">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="75eed-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


