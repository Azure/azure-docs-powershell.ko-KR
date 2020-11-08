---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226438"
---
# <span data-ttu-id="1caff-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="1caff-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="1caff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1caff-102">SYNOPSIS</span></span>
<span data-ttu-id="1caff-103">Application insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="1caff-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="1caff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1caff-104">SYNTAX</span></span>

### <span data-ttu-id="1caff-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1caff-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1caff-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1caff-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1caff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1caff-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1caff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1caff-108">DESCRIPTION</span></span>
<span data-ttu-id="1caff-109">Application insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="1caff-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="1caff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1caff-110">EXAMPLES</span></span>

### <span data-ttu-id="1caff-111">예제 1 application insights 리소스에서 연속 내보내기 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="1caff-112">리소스 그룹 "testgroup"에서 "test" 리소스에 대 한 내보내기 id가 "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" 인 application insights 연속 내보내기 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="1caff-113">변수</span><span class="sxs-lookup"><span data-stu-id="1caff-113">PARAMETERS</span></span>

### <span data-ttu-id="1caff-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1caff-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="1caff-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="1caff-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1caff-116">-DefaultProfile</span></span>
<span data-ttu-id="1caff-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1caff-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="1caff-118">-ExportId</span></span>
<span data-ttu-id="1caff-119">Application Insights 연속 내보내기 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1caff-120">-Name</span></span>
<span data-ttu-id="1caff-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-121">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1caff-122">-PassThru</span></span>
<span data-ttu-id="1caff-123">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="1caff-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-124">This parameter is optional.</span></span> <span data-ttu-id="1caff-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-125">Default value is false.</span></span>

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

### <span data-ttu-id="1caff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1caff-126">-ResourceGroupName</span></span>
<span data-ttu-id="1caff-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1caff-128">-ResourceId</span></span>
<span data-ttu-id="1caff-129">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-130">-확인</span><span class="sxs-lookup"><span data-stu-id="1caff-130">-Confirm</span></span>
<span data-ttu-id="1caff-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1caff-132">-WhatIf</span></span>
<span data-ttu-id="1caff-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1caff-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1caff-135">CommonParameters</span></span>
<span data-ttu-id="1caff-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1caff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1caff-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1caff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1caff-138">입력</span><span class="sxs-lookup"><span data-stu-id="1caff-138">INPUTS</span></span>

### <span data-ttu-id="1caff-139">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="1caff-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="1caff-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1caff-140">System.String</span></span>

## <span data-ttu-id="1caff-141">출력</span><span class="sxs-lookup"><span data-stu-id="1caff-141">OUTPUTS</span></span>

### <span data-ttu-id="1caff-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1caff-142">System.Boolean</span></span>

## <span data-ttu-id="1caff-143">상속자</span><span class="sxs-lookup"><span data-stu-id="1caff-143">NOTES</span></span>

## <span data-ttu-id="1caff-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1caff-144">RELATED LINKS</span></span>
