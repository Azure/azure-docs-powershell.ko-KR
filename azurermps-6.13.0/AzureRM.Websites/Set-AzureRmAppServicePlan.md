---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530811"
---
# <span data-ttu-id="3ce29-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ce29-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="3ce29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce29-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce29-103">Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce29-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce29-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ce29-104">SYNTAX</span></span>

### <span data-ttu-id="3ce29-105">S1</span><span class="sxs-lookup"><span data-stu-id="3ce29-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce29-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="3ce29-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce29-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3ce29-107">DESCRIPTION</span></span>
<span data-ttu-id="3ce29-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce29-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="3ce29-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3ce29-109">EXAMPLES</span></span>

### <span data-ttu-id="3ce29-110">1: 앱 서비스 계획 수정</span><span class="sxs-lookup"><span data-stu-id="3ce29-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="3ce29-111">이 명령은 PerSiteScaling 옵션을 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 라는 App Service 계획에서 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce29-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3ce29-112">변수</span><span class="sxs-lookup"><span data-stu-id="3ce29-112">PARAMETERS</span></span>

### <span data-ttu-id="3ce29-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="3ce29-113">-AdminSiteName</span></span>
<span data-ttu-id="3ce29-114">관리 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="3ce29-114">Admin Site Name</span></span>

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

### <span data-ttu-id="3ce29-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ce29-115">-AppServicePlan</span></span>
<span data-ttu-id="3ce29-116">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="3ce29-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="3ce29-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ce29-117">-AsJob</span></span>
<span data-ttu-id="3ce29-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3ce29-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ce29-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce29-119">-DefaultProfile</span></span>
<span data-ttu-id="3ce29-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ce29-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ce29-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3ce29-121">-Name</span></span>
<span data-ttu-id="3ce29-122">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="3ce29-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="3ce29-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="3ce29-123">-NumberofWorkers</span></span>
<span data-ttu-id="3ce29-124">작업자 수</span><span class="sxs-lookup"><span data-stu-id="3ce29-124">Number Of Workers</span></span>

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

### <span data-ttu-id="3ce29-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="3ce29-125">-PerSiteScaling</span></span>
<span data-ttu-id="3ce29-126">사이트 당 크기 조정 부울</span><span class="sxs-lookup"><span data-stu-id="3ce29-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="3ce29-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce29-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ce29-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3ce29-128">Resource Group Name</span></span>

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

### <span data-ttu-id="3ce29-129">-티어</span><span class="sxs-lookup"><span data-stu-id="3ce29-129">-Tier</span></span>
<span data-ttu-id="3ce29-130">눈금</span><span class="sxs-lookup"><span data-stu-id="3ce29-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce29-131">-. 크기</span><span class="sxs-lookup"><span data-stu-id="3ce29-131">-WorkerSize</span></span>
<span data-ttu-id="3ce29-132">작업자 크기</span><span class="sxs-lookup"><span data-stu-id="3ce29-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce29-133">CommonParameters</span></span>
<span data-ttu-id="3ce29-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce29-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce29-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce29-136">입력</span><span class="sxs-lookup"><span data-stu-id="3ce29-136">INPUTS</span></span>

### <span data-ttu-id="3ce29-137">Microsoft. Azure. p i. i w a p i 관리 계획</span><span class="sxs-lookup"><span data-stu-id="3ce29-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="3ce29-138">매개 변수: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ce29-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="3ce29-139">출력</span><span class="sxs-lookup"><span data-stu-id="3ce29-139">OUTPUTS</span></span>

### <span data-ttu-id="3ce29-140">Microsoft. Azure. p i. i w a p i 관리 계획</span><span class="sxs-lookup"><span data-stu-id="3ce29-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="3ce29-141">상속자</span><span class="sxs-lookup"><span data-stu-id="3ce29-141">NOTES</span></span>

## <span data-ttu-id="3ce29-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ce29-142">RELATED LINKS</span></span>

[<span data-ttu-id="3ce29-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3ce29-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3ce29-144">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3ce29-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3ce29-145">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3ce29-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3ce29-146">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3ce29-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3ce29-147">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3ce29-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3ce29-148">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3ce29-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


