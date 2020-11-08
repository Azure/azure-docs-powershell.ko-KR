---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212456"
---
# <span data-ttu-id="b43fe-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b43fe-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="b43fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b43fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b43fe-103">Azure App Service 계획을 지정 된 지리적 위치에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="b43fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b43fe-104">SYNTAX</span></span>

### <span data-ttu-id="b43fe-105">S1</span><span class="sxs-lookup"><span data-stu-id="b43fe-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b43fe-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="b43fe-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b43fe-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b43fe-107">DESCRIPTION</span></span>
<span data-ttu-id="b43fe-108">**AzAppServicePlan** cmdlet은 지정 된 계층, 작업자 크기 및 작업자 수를 사용 하 여 특정 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="b43fe-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b43fe-109">EXAMPLES</span></span>

### <span data-ttu-id="b43fe-110">예제 1: App Service 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="b43fe-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="b43fe-111">이 명령은 지역 위치 서쪽에 ContosoASP 이라는 리소스 그룹의 WestUS 라는 App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="b43fe-112">명령은 기본 계층을 지정 하 고 두 개의 작은 작업자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="b43fe-113">변수</span><span class="sxs-lookup"><span data-stu-id="b43fe-113">PARAMETERS</span></span>

### <span data-ttu-id="b43fe-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b43fe-114">-AppServicePlan</span></span>
<span data-ttu-id="b43fe-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="b43fe-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b43fe-116">-AseName</span></span>
<span data-ttu-id="b43fe-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="b43fe-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43fe-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b43fe-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b43fe-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b43fe-120">-AsJob</span></span>
<span data-ttu-id="b43fe-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b43fe-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43fe-122">-DefaultProfile</span></span>
<span data-ttu-id="b43fe-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b43fe-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="b43fe-124">-HyperV</span></span>
<span data-ttu-id="b43fe-125">이를 지정 하면 앱 서비스 계획에서 Windows 컨테이너를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-126">-위치</span><span class="sxs-lookup"><span data-stu-id="b43fe-126">-Location</span></span>
<span data-ttu-id="b43fe-127">Location</span><span class="sxs-lookup"><span data-stu-id="b43fe-127">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-128">-이름</span><span class="sxs-lookup"><span data-stu-id="b43fe-128">-Name</span></span>
<span data-ttu-id="b43fe-129">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="b43fe-129">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b43fe-130">-NumberofWorkers</span></span>
<span data-ttu-id="b43fe-131">작업자 수</span><span class="sxs-lookup"><span data-stu-id="b43fe-131">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b43fe-132">-PerSiteScaling</span></span>
<span data-ttu-id="b43fe-133">사이트 단위 크기 조정 사용 여부</span><span class="sxs-lookup"><span data-stu-id="b43fe-133">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43fe-134">-ResourceGroupName</span></span>
<span data-ttu-id="b43fe-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b43fe-135">Resource Group Name</span></span>

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

### <span data-ttu-id="b43fe-136">-티어</span><span class="sxs-lookup"><span data-stu-id="b43fe-136">-Tier</span></span>
<span data-ttu-id="b43fe-137">눈금</span><span class="sxs-lookup"><span data-stu-id="b43fe-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-138">-. 크기</span><span class="sxs-lookup"><span data-stu-id="b43fe-138">-WorkerSize</span></span>
<span data-ttu-id="b43fe-139">웹 작업자의 크기</span><span class="sxs-lookup"><span data-stu-id="b43fe-139">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43fe-140">CommonParameters</span></span>
<span data-ttu-id="b43fe-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43fe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43fe-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43fe-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43fe-143">입력</span><span class="sxs-lookup"><span data-stu-id="b43fe-143">INPUTS</span></span>

### <span data-ttu-id="b43fe-144">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="b43fe-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b43fe-145">출력</span><span class="sxs-lookup"><span data-stu-id="b43fe-145">OUTPUTS</span></span>

### <span data-ttu-id="b43fe-146">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="b43fe-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b43fe-147">상속자</span><span class="sxs-lookup"><span data-stu-id="b43fe-147">NOTES</span></span>

## <span data-ttu-id="b43fe-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b43fe-148">RELATED LINKS</span></span>

[<span data-ttu-id="b43fe-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b43fe-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="b43fe-150">제거-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b43fe-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="b43fe-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b43fe-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


