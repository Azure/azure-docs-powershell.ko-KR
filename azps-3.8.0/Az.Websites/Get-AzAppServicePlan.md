---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878006"
---
# <span data-ttu-id="9a850-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a850-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="9a850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a850-102">SYNOPSIS</span></span>
<span data-ttu-id="9a850-103">지정 된 리소스 그룹에서 Azure App Service 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a850-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="9a850-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a850-104">SYNTAX</span></span>

### <span data-ttu-id="9a850-105">S1</span><span class="sxs-lookup"><span data-stu-id="9a850-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a850-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="9a850-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a850-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9a850-107">DESCRIPTION</span></span>
<span data-ttu-id="9a850-108">**AzAppServicePlan** cmdlet은 지정 된 리소스 그룹에서 Azure App Service 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a850-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="9a850-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9a850-109">EXAMPLES</span></span>

### <span data-ttu-id="9a850-110">예제 1: 리소스 그룹에서 앱 서비스 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a850-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="9a850-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 이라는 App Service 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a850-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="9a850-112">예제 2: 위치에 모든 앱 서비스 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a850-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="9a850-113">이 명령은 "서쪽 US" 지역에 있는 모든 앱 서비스 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a850-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="9a850-114">변수</span><span class="sxs-lookup"><span data-stu-id="9a850-114">PARAMETERS</span></span>

### <span data-ttu-id="9a850-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a850-115">-DefaultProfile</span></span>
<span data-ttu-id="9a850-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a850-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a850-117">-위치</span><span class="sxs-lookup"><span data-stu-id="9a850-117">-Location</span></span>
<span data-ttu-id="9a850-118">Location</span><span class="sxs-lookup"><span data-stu-id="9a850-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a850-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9a850-119">-Name</span></span>
<span data-ttu-id="9a850-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="9a850-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a850-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a850-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a850-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a850-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a850-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a850-123">CommonParameters</span></span>
<span data-ttu-id="9a850-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a850-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a850-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a850-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a850-126">입력</span><span class="sxs-lookup"><span data-stu-id="9a850-126">INPUTS</span></span>

### <span data-ttu-id="9a850-127">않아야</span><span class="sxs-lookup"><span data-stu-id="9a850-127">None</span></span>

## <span data-ttu-id="9a850-128">출력</span><span class="sxs-lookup"><span data-stu-id="9a850-128">OUTPUTS</span></span>

### <span data-ttu-id="9a850-129">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="9a850-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="9a850-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9a850-130">NOTES</span></span>

## <span data-ttu-id="9a850-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a850-131">RELATED LINKS</span></span>

[<span data-ttu-id="9a850-132">새로운 AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a850-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="9a850-133">제거-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a850-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="9a850-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a850-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


