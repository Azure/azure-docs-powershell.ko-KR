---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 0e1c1b9a2aa20546db1306b47b54b18c2b0cd99e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882093"
---
# <span data-ttu-id="f4f23-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f4f23-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="f4f23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f23-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f23-103">Azure 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f23-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4f23-104">SYNTAX</span></span>

### <span data-ttu-id="f4f23-105">S1</span><span class="sxs-lookup"><span data-stu-id="f4f23-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f23-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="f4f23-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f23-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f4f23-107">DESCRIPTION</span></span>
<span data-ttu-id="f4f23-108">**AzureRmWebApp** Cmdlet은 Azure Web App을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f23-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="f4f23-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f4f23-109">EXAMPLES</span></span>

### <span data-ttu-id="f4f23-110">예제 1: 웹 앱 중지</span><span class="sxs-lookup"><span data-stu-id="f4f23-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f4f23-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoWebApp 이라는 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f23-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f4f23-112">변수</span><span class="sxs-lookup"><span data-stu-id="f4f23-112">PARAMETERS</span></span>

### <span data-ttu-id="f4f23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f23-113">-DefaultProfile</span></span>
<span data-ttu-id="f4f23-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4f23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4f23-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f4f23-115">-Name</span></span>
<span data-ttu-id="f4f23-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f4f23-116">WebApp Name</span></span>

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

### <span data-ttu-id="f4f23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f23-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4f23-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f4f23-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f4f23-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="f4f23-119">-WebApp</span></span>
<span data-ttu-id="f4f23-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="f4f23-120">WebApp Object</span></span>

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

### <span data-ttu-id="f4f23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f23-121">CommonParameters</span></span>
<span data-ttu-id="f4f23-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f23-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f23-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f23-124">입력</span><span class="sxs-lookup"><span data-stu-id="f4f23-124">INPUTS</span></span>

### <span data-ttu-id="f4f23-125">Site</span><span class="sxs-lookup"><span data-stu-id="f4f23-125">Site</span></span>
<span data-ttu-id="f4f23-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f23-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f4f23-127">출력</span><span class="sxs-lookup"><span data-stu-id="f4f23-127">OUTPUTS</span></span>

## <span data-ttu-id="f4f23-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f4f23-128">NOTES</span></span>

## <span data-ttu-id="f4f23-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4f23-129">RELATED LINKS</span></span>

[<span data-ttu-id="f4f23-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f4f23-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f4f23-131">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f4f23-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f4f23-132">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f4f23-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f4f23-133">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f4f23-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f4f23-134">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f4f23-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


