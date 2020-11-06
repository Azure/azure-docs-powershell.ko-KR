---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 74f0fcfdcbbc71781debef62becb36018ecb51a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524787"
---
# <span data-ttu-id="6e542-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6e542-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="6e542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e542-102">SYNOPSIS</span></span>
<span data-ttu-id="6e542-103">Azure 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e542-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e542-104">SYNTAX</span></span>

### <span data-ttu-id="6e542-105">S1</span><span class="sxs-lookup"><span data-stu-id="6e542-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e542-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="6e542-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e542-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e542-107">DESCRIPTION</span></span>
<span data-ttu-id="6e542-108">**AzureRmWebApp** Cmdlet은 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e542-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="6e542-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e542-109">EXAMPLES</span></span>

### <span data-ttu-id="6e542-110">예제 1: 웹 앱 시작</span><span class="sxs-lookup"><span data-stu-id="6e542-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="6e542-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e542-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6e542-112">변수</span><span class="sxs-lookup"><span data-stu-id="6e542-112">PARAMETERS</span></span>

### <span data-ttu-id="6e542-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e542-113">-DefaultProfile</span></span>
<span data-ttu-id="6e542-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e542-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e542-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6e542-115">-Name</span></span>
<span data-ttu-id="6e542-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="6e542-116">WebApp Name</span></span>

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

### <span data-ttu-id="6e542-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e542-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e542-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6e542-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6e542-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="6e542-119">-WebApp</span></span>
<span data-ttu-id="6e542-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="6e542-120">WebApp Object</span></span>

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

### <span data-ttu-id="6e542-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e542-121">CommonParameters</span></span>
<span data-ttu-id="6e542-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e542-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e542-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e542-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e542-124">입력</span><span class="sxs-lookup"><span data-stu-id="6e542-124">INPUTS</span></span>

### <span data-ttu-id="6e542-125">Site</span><span class="sxs-lookup"><span data-stu-id="6e542-125">Site</span></span>
<span data-ttu-id="6e542-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e542-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6e542-127">출력</span><span class="sxs-lookup"><span data-stu-id="6e542-127">OUTPUTS</span></span>

## <span data-ttu-id="6e542-128">상속자</span><span class="sxs-lookup"><span data-stu-id="6e542-128">NOTES</span></span>

## <span data-ttu-id="6e542-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e542-129">RELATED LINKS</span></span>

[<span data-ttu-id="6e542-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6e542-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="6e542-131">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6e542-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="6e542-132">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6e542-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="6e542-133">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6e542-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="6e542-134">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6e542-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


