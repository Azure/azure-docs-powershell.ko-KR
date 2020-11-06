---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525104"
---
# <span data-ttu-id="defea-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="defea-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="defea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="defea-102">SYNOPSIS</span></span>
<span data-ttu-id="defea-103">알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="defea-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="defea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="defea-104">SYNTAX</span></span>

### <span data-ttu-id="defea-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="defea-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="defea-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="defea-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="defea-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="defea-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="defea-108">설명은</span><span class="sxs-lookup"><span data-stu-id="defea-108">DESCRIPTION</span></span>
<span data-ttu-id="defea-109">**AzureRmAlertRule** cmdlet은 이름 또는 URI 또는 지정 된 리소스 그룹의 모든 알림 규칙을 기준으로 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="defea-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="defea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="defea-110">EXAMPLES</span></span>

### <span data-ttu-id="defea-111">예제 1: 리소스 그룹에 대 한 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="defea-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="defea-112">이 명령은 Default-CentralUS 이라는 리소스 그룹에 대 한 모든 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="defea-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="defea-113">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에 규칙에 대 한 세부 정보가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="defea-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="defea-114">예제 2: 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="defea-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="defea-115">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="defea-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="defea-116">*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에는 알림 규칙에 대 한 기본 정보만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="defea-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="defea-117">예제 3: 자세한 출력이 있는 이름으로 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="defea-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="defea-118">이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="defea-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="defea-119">*DetailedOutput* 매개 변수를 지정 하면 출력이 자세히 됩니다.</span><span class="sxs-lookup"><span data-stu-id="defea-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="defea-120">변수</span><span class="sxs-lookup"><span data-stu-id="defea-120">PARAMETERS</span></span>

### <span data-ttu-id="defea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defea-121">-DefaultProfile</span></span>
<span data-ttu-id="defea-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="defea-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="defea-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="defea-123">-DetailedOutput</span></span>
<span data-ttu-id="defea-124">출력에 전체 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="defea-124">Displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defea-125">-이름</span><span class="sxs-lookup"><span data-stu-id="defea-125">-Name</span></span>
<span data-ttu-id="defea-126">가져올 알림 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="defea-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defea-127">-ResourceGroupName</span></span>
<span data-ttu-id="defea-128">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="defea-128">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defea-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="defea-129">-TargetResourceId</span></span>
<span data-ttu-id="defea-130">대상 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="defea-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defea-131">CommonParameters</span></span>
<span data-ttu-id="defea-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="defea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defea-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="defea-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defea-134">입력</span><span class="sxs-lookup"><span data-stu-id="defea-134">INPUTS</span></span>

### <span data-ttu-id="defea-135">않아야</span><span class="sxs-lookup"><span data-stu-id="defea-135">None</span></span>
<span data-ttu-id="defea-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="defea-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="defea-137">출력</span><span class="sxs-lookup"><span data-stu-id="defea-137">OUTPUTS</span></span>

### <span data-ttu-id="defea-138">PSAlertRule>를<목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="defea-138">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule></span></span>

## <span data-ttu-id="defea-139">상속자</span><span class="sxs-lookup"><span data-stu-id="defea-139">NOTES</span></span>

## <span data-ttu-id="defea-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="defea-140">RELATED LINKS</span></span>

[<span data-ttu-id="defea-141">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="defea-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="defea-142">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="defea-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="defea-143">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="defea-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="defea-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="defea-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="defea-145">제거-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="defea-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


