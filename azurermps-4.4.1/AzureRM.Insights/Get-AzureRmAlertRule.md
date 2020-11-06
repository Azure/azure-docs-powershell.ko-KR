---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537164"
---
# <span data-ttu-id="b7888-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b7888-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="b7888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7888-102">SYNOPSIS</span></span>
<span data-ttu-id="b7888-103">알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7888-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7888-104">SYNTAX</span></span>

### <span data-ttu-id="b7888-105">Get-AzureRmAlertRule cmdlet에 대 한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7888-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7888-106">Name을 사용 하 여 Get-AzureRmAlertRule cmdlet에 대 한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7888-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7888-107">대상 리소스 uri를 사용 하는 Get-AzureRmAlertRule cmdlet에 대 한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7888-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7888-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b7888-108">DESCRIPTION</span></span>
<span data-ttu-id="b7888-109">**AzureRmAlertRule** cmdlet은 이름 또는 URI 또는 지정 된 리소스 그룹의 모든 알림 규칙을 기준으로 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="b7888-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b7888-110">EXAMPLES</span></span>

### <span data-ttu-id="b7888-111">예제 1: 리소스 그룹에 대 한 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b7888-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="b7888-112">이 명령은 Default-CentralUS 이라는 리소스 그룹에 대 한 모든 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="b7888-113">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에 규칙에 대 한 세부 정보가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="b7888-114">예제 2: 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b7888-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="b7888-115">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b7888-116">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에는 알림 규칙에 대 한 기본 정보만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="b7888-117">예제 3: 자세한 출력이 있는 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b7888-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="b7888-118">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b7888-119">*DetailedOutput* 매개 변수를 지정 하면 출력이 자세히 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="b7888-120">변수</span><span class="sxs-lookup"><span data-stu-id="b7888-120">PARAMETERS</span></span>

### <span data-ttu-id="b7888-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b7888-121">-DetailedOutput</span></span>
<span data-ttu-id="b7888-122">출력에 전체 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="b7888-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b7888-123">-Name</span></span>
<span data-ttu-id="b7888-124">가져올 알림 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7888-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7888-125">-ResourceGroup</span></span>
<span data-ttu-id="b7888-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-126">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7888-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b7888-127">-TargetResourceId</span></span>
<span data-ttu-id="b7888-128">대상 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7888-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7888-129">-DefaultProfile</span></span>
<span data-ttu-id="b7888-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7888-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7888-131">CommonParameters</span></span>
<span data-ttu-id="b7888-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7888-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7888-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7888-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7888-134">입력</span><span class="sxs-lookup"><span data-stu-id="b7888-134">INPUTS</span></span>

## <span data-ttu-id="b7888-135">출력</span><span class="sxs-lookup"><span data-stu-id="b7888-135">OUTPUTS</span></span>

### <span data-ttu-id="b7888-136">System.webserver. List ' 1 [Microsoft Azure. e. 출력 클래스. PSManagementItemDescriptor]</span><span class="sxs-lookup"><span data-stu-id="b7888-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="b7888-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b7888-137">NOTES</span></span>

## <span data-ttu-id="b7888-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7888-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7888-139">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b7888-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="b7888-140">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b7888-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b7888-141">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b7888-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b7888-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b7888-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b7888-143">제거-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b7888-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


