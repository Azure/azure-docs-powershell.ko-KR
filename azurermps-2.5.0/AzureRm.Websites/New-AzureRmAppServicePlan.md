---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: 015a16ec40e7b5159e6082acd47f2583edff1f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881202"
---
# <span data-ttu-id="aad8e-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aad8e-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="aad8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad8e-102">SYNOPSIS</span></span>
<span data-ttu-id="aad8e-103">Azure App Service 계획을 지정 된 지리적 위치에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aad8e-104">SYNTAX</span></span>

### <span data-ttu-id="aad8e-105">S1</span><span class="sxs-lookup"><span data-stu-id="aad8e-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad8e-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="aad8e-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad8e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aad8e-107">DESCRIPTION</span></span>
<span data-ttu-id="aad8e-108">**AzureRmAppServicePlan** cmdlet은 지정 된 계층, 작업자 크기 및 작업자 수를 사용 하 여 특정 지리적 위치에 Azure App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="aad8e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aad8e-109">EXAMPLES</span></span>

### <span data-ttu-id="aad8e-110">예제 1: App Service 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="aad8e-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="aad8e-111">이 명령은 지역 위치 서쪽에 ContosoASP 이라는 리소스 그룹의 WestUS 라는 App Service 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="aad8e-112">명령은 기본 계층을 지정 하 고 두 개의 작은 작업자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="aad8e-113">변수</span><span class="sxs-lookup"><span data-stu-id="aad8e-113">PARAMETERS</span></span>

### <span data-ttu-id="aad8e-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aad8e-114">-AppServicePlan</span></span>
<span data-ttu-id="aad8e-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="aad8e-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="aad8e-116">-AseName</span></span>
<span data-ttu-id="aad8e-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="aad8e-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad8e-118">-AseResourceGroupName</span></span>
<span data-ttu-id="aad8e-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="aad8e-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad8e-120">-DefaultProfile</span></span>
<span data-ttu-id="aad8e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad8e-122">-위치</span><span class="sxs-lookup"><span data-stu-id="aad8e-122">-Location</span></span>
<span data-ttu-id="aad8e-123">Location</span><span class="sxs-lookup"><span data-stu-id="aad8e-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="aad8e-124">-Name</span></span>
<span data-ttu-id="aad8e-125">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="aad8e-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="aad8e-126">-NumberofWorkers</span></span>
<span data-ttu-id="aad8e-127">작업자 수</span><span class="sxs-lookup"><span data-stu-id="aad8e-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="aad8e-128">-PerSiteScaling</span></span>
<span data-ttu-id="aad8e-129">사이트 단위 크기 조정 사용 여부</span><span class="sxs-lookup"><span data-stu-id="aad8e-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad8e-130">-ResourceGroupName</span></span>
<span data-ttu-id="aad8e-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="aad8e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="aad8e-132">-티어</span><span class="sxs-lookup"><span data-stu-id="aad8e-132">-Tier</span></span>
<span data-ttu-id="aad8e-133">눈금</span><span class="sxs-lookup"><span data-stu-id="aad8e-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-134">-. 크기</span><span class="sxs-lookup"><span data-stu-id="aad8e-134">-WorkerSize</span></span>
<span data-ttu-id="aad8e-135">웹 작업자의 크기</span><span class="sxs-lookup"><span data-stu-id="aad8e-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="aad8e-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aad8e-136">-AsJob</span></span>
<span data-ttu-id="aad8e-137">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="aad8e-137">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad8e-138">CommonParameters</span></span>
<span data-ttu-id="aad8e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad8e-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad8e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad8e-141">입력</span><span class="sxs-lookup"><span data-stu-id="aad8e-141">INPUTS</span></span>

### <span data-ttu-id="aad8e-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="aad8e-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="aad8e-143">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad8e-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="aad8e-144">출력</span><span class="sxs-lookup"><span data-stu-id="aad8e-144">OUTPUTS</span></span>

### <span data-ttu-id="aad8e-145">ServerFarmWithRichSku/. m i.</span><span class="sxs-lookup"><span data-stu-id="aad8e-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="aad8e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="aad8e-146">NOTES</span></span>

## <span data-ttu-id="aad8e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aad8e-147">RELATED LINKS</span></span>

[<span data-ttu-id="aad8e-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aad8e-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="aad8e-149">제거-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aad8e-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="aad8e-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aad8e-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)

