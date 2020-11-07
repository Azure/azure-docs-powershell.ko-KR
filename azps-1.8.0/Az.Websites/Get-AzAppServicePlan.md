---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 064ccbcfa94137f5221a5d08e0a06e09328e0b1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698373"
---
# <span data-ttu-id="b8f64-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f64-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="b8f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8f64-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f64-103">지정 된 리소스 그룹에서 Azure App Service 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8f64-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="b8f64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8f64-104">SYNTAX</span></span>

### <span data-ttu-id="b8f64-105">S1</span><span class="sxs-lookup"><span data-stu-id="b8f64-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8f64-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="b8f64-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8f64-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8f64-107">DESCRIPTION</span></span>
<span data-ttu-id="b8f64-108">**AzAppServicePlan** cmdlet은 지정 된 리소스 그룹에서 Azure App Service 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8f64-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="b8f64-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8f64-109">EXAMPLES</span></span>

### <span data-ttu-id="b8f64-110">예제 1: 리소스 그룹에서 앱 서비스 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8f64-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b8f64-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 이라는 App Service 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8f64-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="b8f64-112">예제 2: 위치에 모든 앱 서비스 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8f64-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="b8f64-113">이 명령은 "서쪽 US" 지역에 있는 모든 앱 서비스 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8f64-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="b8f64-114">변수</span><span class="sxs-lookup"><span data-stu-id="b8f64-114">PARAMETERS</span></span>

### <span data-ttu-id="b8f64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f64-115">-DefaultProfile</span></span>
<span data-ttu-id="b8f64-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8f64-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f64-117">-위치</span><span class="sxs-lookup"><span data-stu-id="b8f64-117">-Location</span></span>
<span data-ttu-id="b8f64-118">Location</span><span class="sxs-lookup"><span data-stu-id="b8f64-118">Location</span></span> 

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

### <span data-ttu-id="b8f64-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b8f64-119">-Name</span></span>
<span data-ttu-id="b8f64-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="b8f64-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="b8f64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f64-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8f64-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b8f64-122">Resource Group Name</span></span>

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

### <span data-ttu-id="b8f64-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f64-123">CommonParameters</span></span>
<span data-ttu-id="b8f64-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f64-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f64-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f64-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f64-126">입력</span><span class="sxs-lookup"><span data-stu-id="b8f64-126">INPUTS</span></span>

### <span data-ttu-id="b8f64-127">않아야</span><span class="sxs-lookup"><span data-stu-id="b8f64-127">None</span></span>

## <span data-ttu-id="b8f64-128">출력</span><span class="sxs-lookup"><span data-stu-id="b8f64-128">OUTPUTS</span></span>

### <span data-ttu-id="b8f64-129">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="b8f64-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b8f64-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b8f64-130">NOTES</span></span>

## <span data-ttu-id="b8f64-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8f64-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8f64-132">새로운 AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f64-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="b8f64-133">제거-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f64-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="b8f64-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f64-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


