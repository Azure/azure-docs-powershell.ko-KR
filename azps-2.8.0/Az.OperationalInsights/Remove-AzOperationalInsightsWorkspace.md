---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 9758c0dda8d392100e57909edca310f14d3746af
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93879938"
---
# <span data-ttu-id="abf47-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="abf47-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="abf47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf47-102">SYNOPSIS</span></span>
<span data-ttu-id="abf47-103">작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-103">Removes a workspace.</span></span>

## <span data-ttu-id="abf47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abf47-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf47-105">설명은</span><span class="sxs-lookup"><span data-stu-id="abf47-105">DESCRIPTION</span></span>
<span data-ttu-id="abf47-106">**AzOperationalInsightsWorkspace** cmdlet은 기존 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="abf47-107">이 작업 영역이 만든 시간에 *CustomerId* 매개 변수를 통해 기존 계정에 연결 된 경우에는 Operational Insights 포털에서 원래 계정이 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="abf47-108">예제의</span><span class="sxs-lookup"><span data-stu-id="abf47-108">EXAMPLES</span></span>

### <span data-ttu-id="abf47-109">예제 1: 이름으로 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="abf47-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="abf47-110">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="abf47-111">예제 2: 파이프라인을 사용 하 여 작업 영역을 제거 하 고 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="abf47-112">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고 파이프라인 연산자를 사용 하 여 제거를 **AzOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="abf47-113">*Force* 매개 변수를 지정 했기 때문에 명령에서 작업 영역을 제거 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="abf47-114">변수</span><span class="sxs-lookup"><span data-stu-id="abf47-114">PARAMETERS</span></span>

### <span data-ttu-id="abf47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf47-115">-DefaultProfile</span></span>
<span data-ttu-id="abf47-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="abf47-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abf47-117">-Force</span><span class="sxs-lookup"><span data-stu-id="abf47-117">-Force</span></span>
<span data-ttu-id="abf47-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abf47-119">-이름</span><span class="sxs-lookup"><span data-stu-id="abf47-119">-Name</span></span>
<span data-ttu-id="abf47-120">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-120">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf47-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf47-121">-ResourceGroupName</span></span>
<span data-ttu-id="abf47-122">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-122">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf47-123">-확인</span><span class="sxs-lookup"><span data-stu-id="abf47-123">-Confirm</span></span>
<span data-ttu-id="abf47-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf47-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf47-125">-WhatIf</span></span>
<span data-ttu-id="abf47-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf47-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf47-128">CommonParameters</span></span>
<span data-ttu-id="abf47-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf47-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf47-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf47-131">입력</span><span class="sxs-lookup"><span data-stu-id="abf47-131">INPUTS</span></span>

### <span data-ttu-id="abf47-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="abf47-132">System.String</span></span>

## <span data-ttu-id="abf47-133">출력</span><span class="sxs-lookup"><span data-stu-id="abf47-133">OUTPUTS</span></span>

### <span data-ttu-id="abf47-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="abf47-134">System.Void</span></span>

## <span data-ttu-id="abf47-135">상속자</span><span class="sxs-lookup"><span data-stu-id="abf47-135">NOTES</span></span>

## <span data-ttu-id="abf47-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abf47-136">RELATED LINKS</span></span>

[<span data-ttu-id="abf47-137">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="abf47-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="abf47-138">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="abf47-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


