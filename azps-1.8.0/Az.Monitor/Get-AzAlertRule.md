---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 7164c1f37c3205e3bc2d71f2b820290217aff432
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403105"
---
# <span data-ttu-id="08770-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="08770-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="08770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08770-102">SYNOPSIS</span></span>
<span data-ttu-id="08770-103">경고 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-103">Gets alert rules.</span></span>

## <span data-ttu-id="08770-104">구문</span><span class="sxs-lookup"><span data-stu-id="08770-104">SYNTAX</span></span>

### <span data-ttu-id="08770-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08770-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08770-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="08770-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08770-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="08770-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08770-108">설명</span><span class="sxs-lookup"><span data-stu-id="08770-108">DESCRIPTION</span></span>
<span data-ttu-id="08770-109">**Get-AzAlertRule** cmdlet은 이름 또는 URI 또는 지정된 리소스 그룹의 모든 경고 규칙에 따라 경고 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="08770-110">예제</span><span class="sxs-lookup"><span data-stu-id="08770-110">EXAMPLES</span></span>

### <span data-ttu-id="08770-111">예제 1: 리소스 그룹에 대한 경고 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="08770-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="08770-112">이 명령은 Default-Web-CentralUS라는 리소스 그룹에 대한 모든 경고 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="08770-113">*DetailedOutput* 매개 변수가 지정되지 않은 경우 출력에 규칙에 대한 세부 정보가 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="08770-114">예제 2: 이름으로 경고 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="08770-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="08770-115">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8이라는 경고 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="08770-116">*DetailedOutput* 매개 변수가 지정되지 않은 경우 출력에는 경고 규칙에 대한 기본 정보만 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="08770-117">예제 3: 자세한 출력이 있는 이름으로 경고 규칙 확인</span><span class="sxs-lookup"><span data-stu-id="08770-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="08770-118">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8이라는 경고 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="08770-119">*DetailedOutput* 매개 변수가 지정되어 있으므로 출력이 자세히 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08770-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="08770-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08770-120">PARAMETERS</span></span>

### <span data-ttu-id="08770-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08770-121">-DefaultProfile</span></span>
<span data-ttu-id="08770-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08770-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08770-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="08770-123">-DetailedOutput</span></span>
<span data-ttu-id="08770-124">출력에 전체 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="08770-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08770-125">-Name</span><span class="sxs-lookup"><span data-stu-id="08770-125">-Name</span></span>
<span data-ttu-id="08770-126">얻을 경고 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08770-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08770-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08770-127">-ResourceGroupName</span></span>
<span data-ttu-id="08770-128">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08770-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08770-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="08770-129">-TargetResourceId</span></span>
<span data-ttu-id="08770-130">대상 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08770-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08770-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08770-131">CommonParameters</span></span>
<span data-ttu-id="08770-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08770-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08770-133">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="08770-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08770-134">입력</span><span class="sxs-lookup"><span data-stu-id="08770-134">INPUTS</span></span>

### <span data-ttu-id="08770-135">System.String</span><span class="sxs-lookup"><span data-stu-id="08770-135">System.String</span></span>

### <span data-ttu-id="08770-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08770-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08770-137">출력</span><span class="sxs-lookup"><span data-stu-id="08770-137">OUTPUTS</span></span>

### <span data-ttu-id="08770-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="08770-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="08770-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08770-139">NOTES</span></span>

## <span data-ttu-id="08770-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08770-140">RELATED LINKS</span></span>


[<span data-ttu-id="08770-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="08770-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="08770-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="08770-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="08770-143">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="08770-143">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="08770-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="08770-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


