---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876103"
---
# <span data-ttu-id="aa90d-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aa90d-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="aa90d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa90d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa90d-103">Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa90d-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="aa90d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa90d-104">SYNTAX</span></span>

### <span data-ttu-id="aa90d-105">S1</span><span class="sxs-lookup"><span data-stu-id="aa90d-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa90d-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="aa90d-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa90d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aa90d-107">DESCRIPTION</span></span>
<span data-ttu-id="aa90d-108">**AzAppServicePlan** Cmdlet은 Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa90d-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="aa90d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aa90d-109">EXAMPLES</span></span>

### <span data-ttu-id="aa90d-110">1: 앱 서비스 계획 수정</span><span class="sxs-lookup"><span data-stu-id="aa90d-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="aa90d-111">이 명령은 PerSiteScaling 옵션을 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 라는 App Service 계획에서 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa90d-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="aa90d-112">변수</span><span class="sxs-lookup"><span data-stu-id="aa90d-112">PARAMETERS</span></span>

### <span data-ttu-id="aa90d-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="aa90d-113">-AdminSiteName</span></span>
<span data-ttu-id="aa90d-114">관리 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="aa90d-114">Admin Site Name</span></span>

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

### <span data-ttu-id="aa90d-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="aa90d-115">-AppServicePlan</span></span>
<span data-ttu-id="aa90d-116">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="aa90d-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="aa90d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa90d-117">-DefaultProfile</span></span>
<span data-ttu-id="aa90d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa90d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa90d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="aa90d-119">-Name</span></span>
<span data-ttu-id="aa90d-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="aa90d-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="aa90d-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="aa90d-121">-NumberofWorkers</span></span>
<span data-ttu-id="aa90d-122">작업자 수</span><span class="sxs-lookup"><span data-stu-id="aa90d-122">Number Of Workers</span></span>

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

### <span data-ttu-id="aa90d-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="aa90d-123">-PerSiteScaling</span></span>
<span data-ttu-id="aa90d-124">사이트 당 크기 조정 부울</span><span class="sxs-lookup"><span data-stu-id="aa90d-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="aa90d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa90d-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa90d-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="aa90d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="aa90d-127">-티어</span><span class="sxs-lookup"><span data-stu-id="aa90d-127">-Tier</span></span>
<span data-ttu-id="aa90d-128">눈금</span><span class="sxs-lookup"><span data-stu-id="aa90d-128">Tier</span></span>

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

### <span data-ttu-id="aa90d-129">-. 크기</span><span class="sxs-lookup"><span data-stu-id="aa90d-129">-WorkerSize</span></span>
<span data-ttu-id="aa90d-130">작업자 크기</span><span class="sxs-lookup"><span data-stu-id="aa90d-130">Worker Size</span></span>

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
### <span data-ttu-id="aa90d-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa90d-131">-AsJob</span></span>
<span data-ttu-id="aa90d-132">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="aa90d-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa90d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa90d-133">CommonParameters</span></span>
<span data-ttu-id="aa90d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa90d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa90d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa90d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa90d-136">입력</span><span class="sxs-lookup"><span data-stu-id="aa90d-136">INPUTS</span></span>

### <span data-ttu-id="aa90d-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="aa90d-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="aa90d-138">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa90d-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="aa90d-139">출력</span><span class="sxs-lookup"><span data-stu-id="aa90d-139">OUTPUTS</span></span>

### <span data-ttu-id="aa90d-140">ServerFarmWithRichSku/. m i.</span><span class="sxs-lookup"><span data-stu-id="aa90d-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="aa90d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="aa90d-141">NOTES</span></span>

## <span data-ttu-id="aa90d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa90d-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa90d-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aa90d-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="aa90d-144">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aa90d-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="aa90d-145">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aa90d-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="aa90d-146">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aa90d-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="aa90d-147">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aa90d-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="aa90d-148">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aa90d-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


