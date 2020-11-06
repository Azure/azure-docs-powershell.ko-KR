---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533515"
---
# <span data-ttu-id="1b41f-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1b41f-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="1b41f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b41f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b41f-103">Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b41f-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b41f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b41f-104">SYNTAX</span></span>

### <span data-ttu-id="1b41f-105">S1</span><span class="sxs-lookup"><span data-stu-id="1b41f-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b41f-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="1b41f-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b41f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1b41f-107">DESCRIPTION</span></span>
<span data-ttu-id="1b41f-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b41f-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="1b41f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1b41f-109">EXAMPLES</span></span>

### <span data-ttu-id="1b41f-110">1: 앱 서비스 계획 수정</span><span class="sxs-lookup"><span data-stu-id="1b41f-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="1b41f-111">이 명령은 PerSiteScaling 옵션을 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 라는 App Service 계획에서 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b41f-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1b41f-112">변수</span><span class="sxs-lookup"><span data-stu-id="1b41f-112">PARAMETERS</span></span>

### <span data-ttu-id="1b41f-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="1b41f-113">-AdminSiteName</span></span>
<span data-ttu-id="1b41f-114">관리 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="1b41f-114">Admin Site Name</span></span>

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

### <span data-ttu-id="1b41f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1b41f-115">-AppServicePlan</span></span>
<span data-ttu-id="1b41f-116">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="1b41f-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="1b41f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b41f-117">-DefaultProfile</span></span>
<span data-ttu-id="1b41f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b41f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b41f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1b41f-119">-Name</span></span>
<span data-ttu-id="1b41f-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="1b41f-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="1b41f-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="1b41f-121">-NumberofWorkers</span></span>
<span data-ttu-id="1b41f-122">작업자 수</span><span class="sxs-lookup"><span data-stu-id="1b41f-122">Number Of Workers</span></span>

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

### <span data-ttu-id="1b41f-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="1b41f-123">-PerSiteScaling</span></span>
<span data-ttu-id="1b41f-124">사이트 당 크기 조정 부울</span><span class="sxs-lookup"><span data-stu-id="1b41f-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="1b41f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b41f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b41f-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1b41f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1b41f-127">-티어</span><span class="sxs-lookup"><span data-stu-id="1b41f-127">-Tier</span></span>
<span data-ttu-id="1b41f-128">눈금</span><span class="sxs-lookup"><span data-stu-id="1b41f-128">Tier</span></span>

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

### <span data-ttu-id="1b41f-129">-. 크기</span><span class="sxs-lookup"><span data-stu-id="1b41f-129">-WorkerSize</span></span>
<span data-ttu-id="1b41f-130">작업자 크기</span><span class="sxs-lookup"><span data-stu-id="1b41f-130">Worker Size</span></span>

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
### <span data-ttu-id="1b41f-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b41f-131">-AsJob</span></span>
<span data-ttu-id="1b41f-132">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1b41f-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b41f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b41f-133">CommonParameters</span></span>
<span data-ttu-id="1b41f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b41f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b41f-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b41f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b41f-136">입력</span><span class="sxs-lookup"><span data-stu-id="1b41f-136">INPUTS</span></span>

### <span data-ttu-id="1b41f-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="1b41f-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="1b41f-138">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b41f-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="1b41f-139">출력</span><span class="sxs-lookup"><span data-stu-id="1b41f-139">OUTPUTS</span></span>

### <span data-ttu-id="1b41f-140">ServerFarmWithRichSku/. m i.</span><span class="sxs-lookup"><span data-stu-id="1b41f-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="1b41f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1b41f-141">NOTES</span></span>

## <span data-ttu-id="1b41f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b41f-142">RELATED LINKS</span></span>

[<span data-ttu-id="1b41f-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1b41f-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1b41f-144">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1b41f-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1b41f-145">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1b41f-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1b41f-146">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1b41f-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1b41f-147">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1b41f-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1b41f-148">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1b41f-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


