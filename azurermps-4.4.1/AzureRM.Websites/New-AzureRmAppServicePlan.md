---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711219"
---
# <span data-ttu-id="9a80c-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a80c-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9a80c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a80c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a80c-103">Azure App Service 계획을 지정 된 지리적 위치에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a80c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a80c-104">SYNTAX</span></span>

### <span data-ttu-id="9a80c-105">S1</span><span class="sxs-lookup"><span data-stu-id="9a80c-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a80c-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="9a80c-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a80c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9a80c-107">DESCRIPTION</span></span>
<span data-ttu-id="9a80c-108">**AzureRmAppServicePlan** cmdlet은 지정 된 계층, 작업자 크기 및 작업자 수를 사용 하 여 특정 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="9a80c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9a80c-109">EXAMPLES</span></span>

### <span data-ttu-id="9a80c-110">예제 1: App Service 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="9a80c-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="9a80c-111">이 명령은 지역 위치 서쪽에 ContosoASP 이라는 리소스 그룹의 WestUS 라는 App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="9a80c-112">명령은 기본 계층을 지정 하 고 두 개의 작은 작업자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="9a80c-113">변수</span><span class="sxs-lookup"><span data-stu-id="9a80c-113">PARAMETERS</span></span>

### <span data-ttu-id="9a80c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a80c-114">-AppServicePlan</span></span>
<span data-ttu-id="9a80c-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="9a80c-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a80c-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="9a80c-116">-AseName</span></span>
<span data-ttu-id="9a80c-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="9a80c-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="9a80c-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a80c-118">-AseResourceGroupName</span></span>
<span data-ttu-id="9a80c-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a80c-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9a80c-120">-위치</span><span class="sxs-lookup"><span data-stu-id="9a80c-120">-Location</span></span>
<span data-ttu-id="9a80c-121">Location</span><span class="sxs-lookup"><span data-stu-id="9a80c-121">Location</span></span> 

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

### <span data-ttu-id="9a80c-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9a80c-122">-Name</span></span>
<span data-ttu-id="9a80c-123">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="9a80c-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="9a80c-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="9a80c-124">-NumberofWorkers</span></span>
<span data-ttu-id="9a80c-125">작업자 수</span><span class="sxs-lookup"><span data-stu-id="9a80c-125">Number Of Workers</span></span>

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

### <span data-ttu-id="9a80c-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="9a80c-126">-PerSiteScaling</span></span>
<span data-ttu-id="9a80c-127">사이트 단위 크기 조정 사용 여부</span><span class="sxs-lookup"><span data-stu-id="9a80c-127">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="9a80c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a80c-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a80c-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a80c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="9a80c-130">-티어</span><span class="sxs-lookup"><span data-stu-id="9a80c-130">-Tier</span></span>
<span data-ttu-id="9a80c-131">눈금</span><span class="sxs-lookup"><span data-stu-id="9a80c-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a80c-132">-. 크기</span><span class="sxs-lookup"><span data-stu-id="9a80c-132">-WorkerSize</span></span>
<span data-ttu-id="9a80c-133">웹 작업자의 크기</span><span class="sxs-lookup"><span data-stu-id="9a80c-133">Size of web worker</span></span>

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

### <span data-ttu-id="9a80c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a80c-134">-DefaultProfile</span></span>
<span data-ttu-id="9a80c-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a80c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a80c-136">CommonParameters</span></span>
<span data-ttu-id="9a80c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a80c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a80c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a80c-139">입력</span><span class="sxs-lookup"><span data-stu-id="9a80c-139">INPUTS</span></span>

### <span data-ttu-id="9a80c-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9a80c-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="9a80c-141">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a80c-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="9a80c-142">출력</span><span class="sxs-lookup"><span data-stu-id="9a80c-142">OUTPUTS</span></span>

### <span data-ttu-id="9a80c-143">ServerFarmWithRichSku/. m i.</span><span class="sxs-lookup"><span data-stu-id="9a80c-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="9a80c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="9a80c-144">NOTES</span></span>

## <span data-ttu-id="9a80c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a80c-145">RELATED LINKS</span></span>

[<span data-ttu-id="9a80c-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a80c-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="9a80c-147">제거-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a80c-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="9a80c-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a80c-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


