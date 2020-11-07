---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883062"
---
# <span data-ttu-id="b3ba9-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3ba9-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="b3ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ba9-103">알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ba9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3ba9-104">SYNTAX</span></span>

### <span data-ttu-id="b3ba9-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3ba9-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3ba9-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="b3ba9-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ba9-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="b3ba9-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3ba9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b3ba9-108">DESCRIPTION</span></span>
<span data-ttu-id="b3ba9-109">**AzureRmAlertRule** cmdlet은 이름 또는 URI 또는 지정 된 리소스 그룹의 모든 알림 규칙을 기준으로 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="b3ba9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b3ba9-110">EXAMPLES</span></span>

### <span data-ttu-id="b3ba9-111">예제 1: 리소스 그룹에 대 한 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3ba9-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="b3ba9-112">이 명령은 Default-CentralUS 이라는 리소스 그룹에 대 한 모든 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="b3ba9-113">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에 규칙에 대 한 세부 정보가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="b3ba9-114">예제 2: 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3ba9-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="b3ba9-115">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b3ba9-116">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에는 알림 규칙에 대 한 기본 정보만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="b3ba9-117">예제 3: 자세한 출력이 있는 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3ba9-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="b3ba9-118">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b3ba9-119">*DetailedOutput* 매개 변수를 지정 하면 출력이 자세히 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="b3ba9-120">변수</span><span class="sxs-lookup"><span data-stu-id="b3ba9-120">PARAMETERS</span></span>

### <span data-ttu-id="b3ba9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ba9-121">-DefaultProfile</span></span>
<span data-ttu-id="b3ba9-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b3ba9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3ba9-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b3ba9-123">-DetailedOutput</span></span>
<span data-ttu-id="b3ba9-124">출력에 전체 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="b3ba9-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b3ba9-125">-Name</span></span>
<span data-ttu-id="b3ba9-126">가져올 알림 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="b3ba9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ba9-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3ba9-128">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b3ba9-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ba9-129">-TargetResourceId</span></span>
<span data-ttu-id="b3ba9-130">대상 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="b3ba9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ba9-131">CommonParameters</span></span>
<span data-ttu-id="b3ba9-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ba9-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ba9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ba9-134">입력</span><span class="sxs-lookup"><span data-stu-id="b3ba9-134">INPUTS</span></span>

### <span data-ttu-id="b3ba9-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b3ba9-135">System.String</span></span>

### <span data-ttu-id="b3ba9-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3ba9-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3ba9-137">출력</span><span class="sxs-lookup"><span data-stu-id="b3ba9-137">OUTPUTS</span></span>

### <span data-ttu-id="b3ba9-138">PSAlertRule를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ba9-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="b3ba9-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b3ba9-139">NOTES</span></span>

## <span data-ttu-id="b3ba9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3ba9-140">RELATED LINKS</span></span>



[<span data-ttu-id="b3ba9-141">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3ba9-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b3ba9-142">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3ba9-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b3ba9-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b3ba9-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b3ba9-144">제거-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3ba9-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


