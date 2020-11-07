---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 01774d80ce422c1ac0a48df61d44328b6b5b0105
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875789"
---
# <span data-ttu-id="144c4-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="144c4-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="144c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="144c4-102">SYNOPSIS</span></span>
<span data-ttu-id="144c4-103">알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-103">Gets alert rules.</span></span>

## <span data-ttu-id="144c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="144c4-104">SYNTAX</span></span>

### <span data-ttu-id="144c4-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="144c4-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="144c4-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="144c4-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="144c4-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="144c4-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="144c4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="144c4-108">DESCRIPTION</span></span>
<span data-ttu-id="144c4-109">**AzAlertRule** cmdlet은 이름 또는 URI 또는 지정 된 리소스 그룹의 모든 알림 규칙을 기준으로 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="144c4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="144c4-110">EXAMPLES</span></span>

### <span data-ttu-id="144c4-111">예제 1: 리소스 그룹에 대 한 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="144c4-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="144c4-112">이 명령은 Default-CentralUS 이라는 리소스 그룹에 대 한 모든 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="144c4-113">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에 규칙에 대 한 세부 정보가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="144c4-114">예제 2: 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="144c4-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="144c4-115">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="144c4-116">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에는 알림 규칙에 대 한 기본 정보만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="144c4-117">예제 3: 자세한 출력이 있는 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="144c4-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="144c4-118">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="144c4-119">*DetailedOutput* 매개 변수를 지정 하면 출력이 자세히 됩니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="144c4-120">변수</span><span class="sxs-lookup"><span data-stu-id="144c4-120">PARAMETERS</span></span>

### <span data-ttu-id="144c4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144c4-121">-DefaultProfile</span></span>
<span data-ttu-id="144c4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="144c4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="144c4-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="144c4-123">-DetailedOutput</span></span>
<span data-ttu-id="144c4-124">출력에 전체 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="144c4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="144c4-125">-Name</span></span>
<span data-ttu-id="144c4-126">가져올 알림 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="144c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="144c4-128">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="144c4-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="144c4-129">-TargetResourceId</span></span>
<span data-ttu-id="144c4-130">대상 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="144c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144c4-131">CommonParameters</span></span>
<span data-ttu-id="144c4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144c4-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="144c4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144c4-134">입력</span><span class="sxs-lookup"><span data-stu-id="144c4-134">INPUTS</span></span>

### <span data-ttu-id="144c4-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="144c4-135">System.String</span></span>

### <span data-ttu-id="144c4-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="144c4-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="144c4-137">출력</span><span class="sxs-lookup"><span data-stu-id="144c4-137">OUTPUTS</span></span>

### <span data-ttu-id="144c4-138">PSAlertRule를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="144c4-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="144c4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="144c4-139">NOTES</span></span>

## <span data-ttu-id="144c4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="144c4-140">RELATED LINKS</span></span>

[<span data-ttu-id="144c4-141">추가-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="144c4-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="144c4-142">추가-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="144c4-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="144c4-143">추가-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="144c4-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="144c4-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="144c4-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="144c4-145">제거-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="144c4-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


