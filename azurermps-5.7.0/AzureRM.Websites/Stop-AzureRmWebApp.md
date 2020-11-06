---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: d1e4e029676eadec3f793aff99a2d68983891f2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534532"
---
# <span data-ttu-id="74776-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74776-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="74776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74776-102">SYNOPSIS</span></span>
<span data-ttu-id="74776-103">Azure 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="74776-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74776-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74776-104">SYNTAX</span></span>

### <span data-ttu-id="74776-105">S1</span><span class="sxs-lookup"><span data-stu-id="74776-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74776-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="74776-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74776-107">설명은</span><span class="sxs-lookup"><span data-stu-id="74776-107">DESCRIPTION</span></span>
<span data-ttu-id="74776-108">**AzureRmWebApp** Cmdlet은 Azure Web App을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="74776-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="74776-109">예제의</span><span class="sxs-lookup"><span data-stu-id="74776-109">EXAMPLES</span></span>

### <span data-ttu-id="74776-110">예제 1: 웹 앱 중지</span><span class="sxs-lookup"><span data-stu-id="74776-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="74776-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoWebApp 이라는 웹 앱을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="74776-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="74776-112">변수</span><span class="sxs-lookup"><span data-stu-id="74776-112">PARAMETERS</span></span>

### <span data-ttu-id="74776-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74776-113">-DefaultProfile</span></span>
<span data-ttu-id="74776-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74776-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74776-115">-이름</span><span class="sxs-lookup"><span data-stu-id="74776-115">-Name</span></span>
<span data-ttu-id="74776-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="74776-116">WebApp Name</span></span>

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

### <span data-ttu-id="74776-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74776-117">-ResourceGroupName</span></span>
<span data-ttu-id="74776-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="74776-118">Resource Group Name</span></span>

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

### <span data-ttu-id="74776-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="74776-119">-WebApp</span></span>
<span data-ttu-id="74776-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="74776-120">WebApp Object</span></span>

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

### <span data-ttu-id="74776-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74776-121">CommonParameters</span></span>
<span data-ttu-id="74776-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74776-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74776-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74776-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74776-124">입력</span><span class="sxs-lookup"><span data-stu-id="74776-124">INPUTS</span></span>

### <span data-ttu-id="74776-125">Site</span><span class="sxs-lookup"><span data-stu-id="74776-125">Site</span></span>
<span data-ttu-id="74776-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="74776-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="74776-127">출력</span><span class="sxs-lookup"><span data-stu-id="74776-127">OUTPUTS</span></span>

## <span data-ttu-id="74776-128">상속자</span><span class="sxs-lookup"><span data-stu-id="74776-128">NOTES</span></span>

## <span data-ttu-id="74776-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74776-129">RELATED LINKS</span></span>

[<span data-ttu-id="74776-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74776-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="74776-131">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74776-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="74776-132">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74776-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="74776-133">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74776-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="74776-134">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="74776-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


