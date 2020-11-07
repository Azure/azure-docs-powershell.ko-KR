---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874219"
---
# <span data-ttu-id="ea065-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ea065-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="ea065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea065-102">SYNOPSIS</span></span>
<span data-ttu-id="ea065-103">Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea065-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ea065-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea065-104">SYNTAX</span></span>

### <span data-ttu-id="ea065-105">S1</span><span class="sxs-lookup"><span data-stu-id="ea065-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea065-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="ea065-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea065-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea065-107">DESCRIPTION</span></span>
<span data-ttu-id="ea065-108">**AzAppServicePlan** Cmdlet은 Azure App Service 계획을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea065-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ea065-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ea065-109">EXAMPLES</span></span>

### <span data-ttu-id="ea065-110">1: 앱 서비스 계획 수정</span><span class="sxs-lookup"><span data-stu-id="ea065-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="ea065-111">이 명령은 PerSiteScaling 옵션을 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 라는 App Service 계획에서 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea065-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ea065-112">변수</span><span class="sxs-lookup"><span data-stu-id="ea065-112">PARAMETERS</span></span>

### <span data-ttu-id="ea065-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="ea065-113">-AdminSiteName</span></span>
<span data-ttu-id="ea065-114">관리 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="ea065-114">Admin Site Name</span></span>

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

### <span data-ttu-id="ea065-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ea065-115">-AppServicePlan</span></span>
<span data-ttu-id="ea065-116">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="ea065-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="ea065-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea065-117">-AsJob</span></span>
<span data-ttu-id="ea065-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ea065-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea065-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea065-119">-DefaultProfile</span></span>
<span data-ttu-id="ea065-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea065-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea065-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ea065-121">-Name</span></span>
<span data-ttu-id="ea065-122">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="ea065-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="ea065-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ea065-123">-NumberofWorkers</span></span>
<span data-ttu-id="ea065-124">작업자 수</span><span class="sxs-lookup"><span data-stu-id="ea065-124">Number Of Workers</span></span>

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

### <span data-ttu-id="ea065-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ea065-125">-PerSiteScaling</span></span>
<span data-ttu-id="ea065-126">사이트 당 크기 조정 부울</span><span class="sxs-lookup"><span data-stu-id="ea065-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="ea065-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea065-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea065-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ea065-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ea065-129">-티어</span><span class="sxs-lookup"><span data-stu-id="ea065-129">-Tier</span></span>
<span data-ttu-id="ea065-130">눈금</span><span class="sxs-lookup"><span data-stu-id="ea065-130">Tier</span></span>

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

### <span data-ttu-id="ea065-131">-. 크기</span><span class="sxs-lookup"><span data-stu-id="ea065-131">-WorkerSize</span></span>
<span data-ttu-id="ea065-132">작업자 크기</span><span class="sxs-lookup"><span data-stu-id="ea065-132">Worker Size</span></span>

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

### <span data-ttu-id="ea065-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea065-133">CommonParameters</span></span>
<span data-ttu-id="ea065-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea065-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea065-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea065-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea065-136">입력</span><span class="sxs-lookup"><span data-stu-id="ea065-136">INPUTS</span></span>

### <span data-ttu-id="ea065-137">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="ea065-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ea065-138">출력</span><span class="sxs-lookup"><span data-stu-id="ea065-138">OUTPUTS</span></span>

### <span data-ttu-id="ea065-139">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="ea065-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ea065-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ea065-140">NOTES</span></span>

## <span data-ttu-id="ea065-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea065-141">RELATED LINKS</span></span>

[<span data-ttu-id="ea065-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea065-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ea065-143">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea065-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ea065-144">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea065-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ea065-145">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea065-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ea065-146">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea065-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ea065-147">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea065-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


