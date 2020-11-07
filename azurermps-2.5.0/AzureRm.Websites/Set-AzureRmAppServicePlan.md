---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: eac153c22a576686feb15b75f3180ed4fb12ec94
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882418"
---
# <span data-ttu-id="8f369-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8f369-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="8f369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f369-102">SYNOPSIS</span></span>
<span data-ttu-id="8f369-103">Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f369-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f369-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f369-104">SYNTAX</span></span>

### <span data-ttu-id="8f369-105">S1</span><span class="sxs-lookup"><span data-stu-id="8f369-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f369-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="8f369-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f369-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8f369-107">DESCRIPTION</span></span>
<span data-ttu-id="8f369-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f369-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="8f369-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8f369-109">EXAMPLES</span></span>

### <span data-ttu-id="8f369-110">1: 앱 서비스 계획 수정</span><span class="sxs-lookup"><span data-stu-id="8f369-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="8f369-111">이 명령은 PerSiteScaling 옵션을 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 라는 App Service 계획에서 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f369-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8f369-112">변수</span><span class="sxs-lookup"><span data-stu-id="8f369-112">PARAMETERS</span></span>

### <span data-ttu-id="8f369-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="8f369-113">-AdminSiteName</span></span>
<span data-ttu-id="8f369-114">관리 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="8f369-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f369-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8f369-115">-AppServicePlan</span></span>
<span data-ttu-id="8f369-116">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="8f369-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f369-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f369-117">-DefaultProfile</span></span>
<span data-ttu-id="8f369-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f369-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f369-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8f369-119">-Name</span></span>
<span data-ttu-id="8f369-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="8f369-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="8f369-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="8f369-121">-NumberofWorkers</span></span>
<span data-ttu-id="8f369-122">작업자 수</span><span class="sxs-lookup"><span data-stu-id="8f369-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f369-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="8f369-123">-PerSiteScaling</span></span>
<span data-ttu-id="8f369-124">사이트 당 크기 조정 부울</span><span class="sxs-lookup"><span data-stu-id="8f369-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f369-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f369-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f369-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8f369-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8f369-127">-티어</span><span class="sxs-lookup"><span data-stu-id="8f369-127">-Tier</span></span>
<span data-ttu-id="8f369-128">눈금</span><span class="sxs-lookup"><span data-stu-id="8f369-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f369-129">-. 크기</span><span class="sxs-lookup"><span data-stu-id="8f369-129">-WorkerSize</span></span>
<span data-ttu-id="8f369-130">작업자 크기</span><span class="sxs-lookup"><span data-stu-id="8f369-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="8f369-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f369-131">-AsJob</span></span>
<span data-ttu-id="8f369-132">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8f369-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f369-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f369-133">CommonParameters</span></span>
<span data-ttu-id="8f369-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f369-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f369-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f369-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f369-136">입력</span><span class="sxs-lookup"><span data-stu-id="8f369-136">INPUTS</span></span>

### <span data-ttu-id="8f369-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8f369-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="8f369-138">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f369-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="8f369-139">출력</span><span class="sxs-lookup"><span data-stu-id="8f369-139">OUTPUTS</span></span>

### <span data-ttu-id="8f369-140">ServerFarmWithRichSku/. m i.</span><span class="sxs-lookup"><span data-stu-id="8f369-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="8f369-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8f369-141">NOTES</span></span>

## <span data-ttu-id="8f369-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f369-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f369-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f369-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="8f369-144">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f369-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="8f369-145">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f369-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="8f369-146">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f369-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="8f369-147">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f369-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="8f369-148">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f369-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


