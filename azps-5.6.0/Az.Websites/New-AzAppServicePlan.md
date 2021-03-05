---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011131"
---
# <span data-ttu-id="9f983-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="9f983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f983-102">SYNOPSIS</span></span>
<span data-ttu-id="9f983-103">지정한 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="9f983-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f983-104">SYNTAX</span></span>

### <span data-ttu-id="9f983-105">S1</span><span class="sxs-lookup"><span data-stu-id="9f983-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f983-106">S2</span><span class="sxs-lookup"><span data-stu-id="9f983-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f983-107">설명</span><span class="sxs-lookup"><span data-stu-id="9f983-107">DESCRIPTION</span></span>
<span data-ttu-id="9f983-108">**New-AzAppServicePlan** cmdlet은 지정된 계층, 작업자 크기 및 작업자 수가 지정된 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="9f983-109">예제</span><span class="sxs-lookup"><span data-stu-id="9f983-109">EXAMPLES</span></span>

### <span data-ttu-id="9f983-110">예제 1: App Service 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="9f983-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="9f983-111">이 명령은 미국 서부 지역 위치의 Default-Web-WestUS라는 리소스 그룹에 ContosoASP라는 App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="9f983-112">명령은 기본 계층을 지정하고 두 개의 작은 작업자를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="9f983-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f983-113">PARAMETERS</span></span>

### <span data-ttu-id="9f983-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-114">-AppServicePlan</span></span>
<span data-ttu-id="9f983-115">App Service Plan 개체</span><span class="sxs-lookup"><span data-stu-id="9f983-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="9f983-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="9f983-116">-AseName</span></span>
<span data-ttu-id="9f983-117">App Service 환경 이름</span><span class="sxs-lookup"><span data-stu-id="9f983-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="9f983-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f983-118">-AseResourceGroupName</span></span>
<span data-ttu-id="9f983-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9f983-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9f983-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f983-120">-AsJob</span></span>
<span data-ttu-id="9f983-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9f983-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f983-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f983-122">-DefaultProfile</span></span>
<span data-ttu-id="9f983-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f983-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="9f983-124">-HyperV</span></span>
<span data-ttu-id="9f983-125">이를 지정하면 App Service 계획이 Windows 컨테이너를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="9f983-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="9f983-126">-Linux</span></span>
<span data-ttu-id="9f983-127">이를 지정하면 App Service 계획이 Linux 컨테이너를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="9f983-128">-Location</span><span class="sxs-lookup"><span data-stu-id="9f983-128">-Location</span></span>
<span data-ttu-id="9f983-129">위치</span><span class="sxs-lookup"><span data-stu-id="9f983-129">Location</span></span> 

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

### <span data-ttu-id="9f983-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9f983-130">-Name</span></span>
<span data-ttu-id="9f983-131">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="9f983-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="9f983-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="9f983-132">-NumberofWorkers</span></span>
<span data-ttu-id="9f983-133">작업자 수</span><span class="sxs-lookup"><span data-stu-id="9f983-133">Number Of Workers</span></span>

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

### <span data-ttu-id="9f983-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="9f983-134">-PerSiteScaling</span></span>
<span data-ttu-id="9f983-135">사이트당 크기 조정을 사용하도록 설정할지 여부</span><span class="sxs-lookup"><span data-stu-id="9f983-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="9f983-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f983-136">-ResourceGroupName</span></span>
<span data-ttu-id="9f983-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9f983-137">Resource Group Name</span></span>

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

### <span data-ttu-id="9f983-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f983-138">-Tag</span></span>
<span data-ttu-id="9f983-139">태그는 리소스를 분류할 수 있는 이름/값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f983-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="9f983-140">-Tier</span></span>
<span data-ttu-id="9f983-141">계층</span><span class="sxs-lookup"><span data-stu-id="9f983-141">Tier</span></span>

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

### <span data-ttu-id="9f983-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="9f983-142">-WorkerSize</span></span>
<span data-ttu-id="9f983-143">웹 작업자 크기</span><span class="sxs-lookup"><span data-stu-id="9f983-143">Size of web worker</span></span>

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

### <span data-ttu-id="9f983-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f983-144">CommonParameters</span></span>
<span data-ttu-id="9f983-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f983-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f983-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f983-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f983-147">입력</span><span class="sxs-lookup"><span data-stu-id="9f983-147">INPUTS</span></span>

### <span data-ttu-id="9f983-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="9f983-149">출력</span><span class="sxs-lookup"><span data-stu-id="9f983-149">OUTPUTS</span></span>

### <span data-ttu-id="9f983-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="9f983-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f983-151">NOTES</span></span>

## <span data-ttu-id="9f983-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f983-152">RELATED LINKS</span></span>

[<span data-ttu-id="9f983-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="9f983-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="9f983-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f983-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


