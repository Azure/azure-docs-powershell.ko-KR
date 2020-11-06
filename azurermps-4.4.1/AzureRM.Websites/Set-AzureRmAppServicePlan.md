---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528171"
---
# <span data-ttu-id="f63a6-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f63a6-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="f63a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f63a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f63a6-103">Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63a6-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f63a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f63a6-104">SYNTAX</span></span>

### <span data-ttu-id="f63a6-105">S1</span><span class="sxs-lookup"><span data-stu-id="f63a6-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f63a6-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="f63a6-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f63a6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f63a6-107">DESCRIPTION</span></span>
<span data-ttu-id="f63a6-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63a6-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="f63a6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f63a6-109">EXAMPLES</span></span>

### <span data-ttu-id="f63a6-110">1: 앱 서비스 계획 수정</span><span class="sxs-lookup"><span data-stu-id="f63a6-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="f63a6-111">이 명령은 PerSiteScaling 옵션을 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 라는 App Service 계획에서 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63a6-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f63a6-112">변수</span><span class="sxs-lookup"><span data-stu-id="f63a6-112">PARAMETERS</span></span>

### <span data-ttu-id="f63a6-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="f63a6-113">-AdminSiteName</span></span>
<span data-ttu-id="f63a6-114">관리 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="f63a6-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63a6-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f63a6-115">-AppServicePlan</span></span>
<span data-ttu-id="f63a6-116">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="f63a6-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="f63a6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f63a6-117">-Name</span></span>
<span data-ttu-id="f63a6-118">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="f63a6-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="f63a6-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="f63a6-119">-NumberofWorkers</span></span>
<span data-ttu-id="f63a6-120">작업자 수</span><span class="sxs-lookup"><span data-stu-id="f63a6-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63a6-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="f63a6-121">-PerSiteScaling</span></span>
<span data-ttu-id="f63a6-122">사이트 당 크기 조정 부울</span><span class="sxs-lookup"><span data-stu-id="f63a6-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f63a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="f63a6-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f63a6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f63a6-125">-티어</span><span class="sxs-lookup"><span data-stu-id="f63a6-125">-Tier</span></span>
<span data-ttu-id="f63a6-126">눈금</span><span class="sxs-lookup"><span data-stu-id="f63a6-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63a6-127">-. 크기</span><span class="sxs-lookup"><span data-stu-id="f63a6-127">-WorkerSize</span></span>
<span data-ttu-id="f63a6-128">작업자 크기</span><span class="sxs-lookup"><span data-stu-id="f63a6-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63a6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63a6-129">-DefaultProfile</span></span>
<span data-ttu-id="f63a6-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f63a6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f63a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63a6-131">CommonParameters</span></span>
<span data-ttu-id="f63a6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63a6-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f63a6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63a6-134">입력</span><span class="sxs-lookup"><span data-stu-id="f63a6-134">INPUTS</span></span>

### <span data-ttu-id="f63a6-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="f63a6-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="f63a6-136">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63a6-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="f63a6-137">출력</span><span class="sxs-lookup"><span data-stu-id="f63a6-137">OUTPUTS</span></span>

### <span data-ttu-id="f63a6-138">ServerFarmWithRichSku/. m i.</span><span class="sxs-lookup"><span data-stu-id="f63a6-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="f63a6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f63a6-139">NOTES</span></span>

## <span data-ttu-id="f63a6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f63a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="f63a6-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f63a6-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f63a6-142">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f63a6-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f63a6-143">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f63a6-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f63a6-144">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f63a6-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f63a6-145">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f63a6-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f63a6-146">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f63a6-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


