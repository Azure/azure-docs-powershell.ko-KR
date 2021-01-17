---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491464"
---
# <span data-ttu-id="22fef-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="22fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22fef-102">SYNOPSIS</span></span>
<span data-ttu-id="22fef-103">지정한 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="22fef-104">구문</span><span class="sxs-lookup"><span data-stu-id="22fef-104">SYNTAX</span></span>

### <span data-ttu-id="22fef-105">S1</span><span class="sxs-lookup"><span data-stu-id="22fef-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22fef-106">S2</span><span class="sxs-lookup"><span data-stu-id="22fef-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22fef-107">설명</span><span class="sxs-lookup"><span data-stu-id="22fef-107">DESCRIPTION</span></span>
<span data-ttu-id="22fef-108">**New-AzAppServicePlan** cmdlet은 지정된 계층, 작업자 크기 및 작업자 수를 사용하여 지정된 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="22fef-109">예제</span><span class="sxs-lookup"><span data-stu-id="22fef-109">EXAMPLES</span></span>

### <span data-ttu-id="22fef-110">예제 1: App Service 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="22fef-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="22fef-111">이 명령은 미국 서부 지역 위치의 Default-Web-WestUS 리소스 그룹에 ContosoASP라는 App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="22fef-112">이 명령은 기본 계층을 지정하고 두 개의 작은 작업자를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="22fef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22fef-113">PARAMETERS</span></span>

### <span data-ttu-id="22fef-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-114">-AppServicePlan</span></span>
<span data-ttu-id="22fef-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="22fef-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="22fef-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="22fef-116">-AseName</span></span>
<span data-ttu-id="22fef-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="22fef-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="22fef-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22fef-118">-AseResourceGroupName</span></span>
<span data-ttu-id="22fef-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="22fef-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="22fef-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22fef-120">-AsJob</span></span>
<span data-ttu-id="22fef-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="22fef-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22fef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22fef-122">-DefaultProfile</span></span>
<span data-ttu-id="22fef-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22fef-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="22fef-124">-HyperV</span></span>
<span data-ttu-id="22fef-125">이를 지정합니다. App Service 계획은 Windows 컨테이너를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="22fef-126">-Location</span><span class="sxs-lookup"><span data-stu-id="22fef-126">-Location</span></span>
<span data-ttu-id="22fef-127">위치</span><span class="sxs-lookup"><span data-stu-id="22fef-127">Location</span></span> 

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

### <span data-ttu-id="22fef-128">-Name</span><span class="sxs-lookup"><span data-stu-id="22fef-128">-Name</span></span>
<span data-ttu-id="22fef-129">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="22fef-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="22fef-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="22fef-130">-NumberofWorkers</span></span>
<span data-ttu-id="22fef-131">작업자 수</span><span class="sxs-lookup"><span data-stu-id="22fef-131">Number Of Workers</span></span>

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

### <span data-ttu-id="22fef-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="22fef-132">-PerSiteScaling</span></span>
<span data-ttu-id="22fef-133">사이트 크기 조정을 사용하도록 설정할지 여부</span><span class="sxs-lookup"><span data-stu-id="22fef-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="22fef-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22fef-134">-ResourceGroupName</span></span>
<span data-ttu-id="22fef-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="22fef-135">Resource Group Name</span></span>

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

### <span data-ttu-id="22fef-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="22fef-136">-Tier</span></span>
<span data-ttu-id="22fef-137">계층</span><span class="sxs-lookup"><span data-stu-id="22fef-137">Tier</span></span>

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

### <span data-ttu-id="22fef-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="22fef-138">-WorkerSize</span></span>
<span data-ttu-id="22fef-139">웹 작업의 크기</span><span class="sxs-lookup"><span data-stu-id="22fef-139">Size of web worker</span></span>

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

### <span data-ttu-id="22fef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22fef-140">CommonParameters</span></span>
<span data-ttu-id="22fef-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22fef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22fef-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="22fef-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22fef-143">입력</span><span class="sxs-lookup"><span data-stu-id="22fef-143">INPUTS</span></span>

### <span data-ttu-id="22fef-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="22fef-145">출력</span><span class="sxs-lookup"><span data-stu-id="22fef-145">OUTPUTS</span></span>

### <span data-ttu-id="22fef-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="22fef-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22fef-147">NOTES</span></span>

## <span data-ttu-id="22fef-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22fef-148">RELATED LINKS</span></span>

[<span data-ttu-id="22fef-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="22fef-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="22fef-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22fef-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


