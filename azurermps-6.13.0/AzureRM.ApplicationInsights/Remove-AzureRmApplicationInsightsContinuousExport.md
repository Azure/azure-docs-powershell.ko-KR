---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: b9a26a1279b89609728837def1997ac5735ddaea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528670"
---
# <span data-ttu-id="069ec-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="069ec-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="069ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="069ec-102">SYNOPSIS</span></span>
<span data-ttu-id="069ec-103">Application insights 리소스에서 cotinuous 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="069ec-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="069ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="069ec-104">SYNTAX</span></span>

### <span data-ttu-id="069ec-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="069ec-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="069ec-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="069ec-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="069ec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="069ec-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="069ec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="069ec-108">DESCRIPTION</span></span>
<span data-ttu-id="069ec-109">Application insights 리소스에서 cotinuous 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="069ec-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="069ec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="069ec-110">EXAMPLES</span></span>

### <span data-ttu-id="069ec-111">예제 1 application insights 리소스에서 cotinuous 내보내기 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="069ec-112">리소스 그룹 "testgroup"에서 "test" 리소스에 대 한 내보내기 id가 "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" 인 application insights 연속 내보내기 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="069ec-113">변수</span><span class="sxs-lookup"><span data-stu-id="069ec-113">PARAMETERS</span></span>

### <span data-ttu-id="069ec-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="069ec-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="069ec-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="069ec-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="069ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="069ec-116">-DefaultProfile</span></span>
<span data-ttu-id="069ec-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="069ec-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="069ec-118">-ExportId</span></span>
<span data-ttu-id="069ec-119">Application Insights 연속 내보내기 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="069ec-120">-이름</span><span class="sxs-lookup"><span data-stu-id="069ec-120">-Name</span></span>
<span data-ttu-id="069ec-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="069ec-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="069ec-122">-PassThru</span></span>
<span data-ttu-id="069ec-123">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="069ec-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-124">This parameter is optional.</span></span> <span data-ttu-id="069ec-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-125">Default value is false.</span></span>

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

### <span data-ttu-id="069ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="069ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="069ec-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="069ec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="069ec-128">-ResourceId</span></span>
<span data-ttu-id="069ec-129">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="069ec-130">-확인</span><span class="sxs-lookup"><span data-stu-id="069ec-130">-Confirm</span></span>
<span data-ttu-id="069ec-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="069ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="069ec-132">-WhatIf</span></span>
<span data-ttu-id="069ec-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="069ec-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="069ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="069ec-135">CommonParameters</span></span>
<span data-ttu-id="069ec-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="069ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="069ec-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="069ec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="069ec-138">입력</span><span class="sxs-lookup"><span data-stu-id="069ec-138">INPUTS</span></span>

### <span data-ttu-id="069ec-139">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="069ec-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="069ec-140">매개 변수: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="069ec-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="069ec-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="069ec-141">System.String</span></span>

## <span data-ttu-id="069ec-142">출력</span><span class="sxs-lookup"><span data-stu-id="069ec-142">OUTPUTS</span></span>

### <span data-ttu-id="069ec-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="069ec-143">System.Boolean</span></span>

## <span data-ttu-id="069ec-144">상속자</span><span class="sxs-lookup"><span data-stu-id="069ec-144">NOTES</span></span>

## <span data-ttu-id="069ec-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="069ec-145">RELATED LINKS</span></span>
