---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380794"
---
# <span data-ttu-id="5f380-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f380-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="5f380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f380-102">SYNOPSIS</span></span>
<span data-ttu-id="5f380-103">지정된 리소스 그룹에서 Azure App Service 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f380-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="5f380-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f380-104">SYNTAX</span></span>

### <span data-ttu-id="5f380-105">S1</span><span class="sxs-lookup"><span data-stu-id="5f380-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f380-106">S2</span><span class="sxs-lookup"><span data-stu-id="5f380-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f380-107">설명</span><span class="sxs-lookup"><span data-stu-id="5f380-107">DESCRIPTION</span></span>
<span data-ttu-id="5f380-108">**Get-AzAppServicePlan** cmdlet은 지정된 리소스 그룹에서 Azure App Service 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f380-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="5f380-109">예제</span><span class="sxs-lookup"><span data-stu-id="5f380-109">EXAMPLES</span></span>

### <span data-ttu-id="5f380-110">예제 1: 리소스 그룹에서 App Service 계획 다운로드</span><span class="sxs-lookup"><span data-stu-id="5f380-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="5f380-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoASP라는 App Service 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f380-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="5f380-112">예제 2: 한 위치에서 모든 App Service 계획 다운로드</span><span class="sxs-lookup"><span data-stu-id="5f380-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="5f380-113">이 명령은 "미국 서부" 지역에 있는 모든 App Service 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f380-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="5f380-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f380-114">PARAMETERS</span></span>

### <span data-ttu-id="5f380-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f380-115">-DefaultProfile</span></span>
<span data-ttu-id="5f380-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f380-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f380-117">-Location</span><span class="sxs-lookup"><span data-stu-id="5f380-117">-Location</span></span>
<span data-ttu-id="5f380-118">위치</span><span class="sxs-lookup"><span data-stu-id="5f380-118">Location</span></span> 

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

### <span data-ttu-id="5f380-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5f380-119">-Name</span></span>
<span data-ttu-id="5f380-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="5f380-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="5f380-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f380-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f380-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5f380-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5f380-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f380-123">CommonParameters</span></span>
<span data-ttu-id="5f380-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f380-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f380-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5f380-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f380-126">입력</span><span class="sxs-lookup"><span data-stu-id="5f380-126">INPUTS</span></span>

### <span data-ttu-id="5f380-127">없음</span><span class="sxs-lookup"><span data-stu-id="5f380-127">None</span></span>

## <span data-ttu-id="5f380-128">출력</span><span class="sxs-lookup"><span data-stu-id="5f380-128">OUTPUTS</span></span>

### <span data-ttu-id="5f380-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f380-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="5f380-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f380-130">NOTES</span></span>

## <span data-ttu-id="5f380-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f380-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f380-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f380-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="5f380-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f380-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="5f380-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f380-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


