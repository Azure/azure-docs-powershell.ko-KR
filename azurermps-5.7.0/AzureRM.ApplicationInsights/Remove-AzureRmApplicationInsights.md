---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703592"
---
# <span data-ttu-id="f8e55-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f8e55-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="f8e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e55-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e55-103">Application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="f8e55-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8e55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8e55-104">SYNTAX</span></span>

### <span data-ttu-id="f8e55-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8e55-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8e55-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8e55-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8e55-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8e55-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8e55-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f8e55-108">DESCRIPTION</span></span>
<span data-ttu-id="f8e55-109">Application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="f8e55-109">Remove an application insights resource</span></span>

## <span data-ttu-id="f8e55-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f8e55-110">EXAMPLES</span></span>

### <span data-ttu-id="f8e55-111">예제 1 application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="f8e55-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="f8e55-112">리소스 그룹 "testgroup"에서 "test" 라는 applciation insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="f8e55-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f8e55-113">변수</span><span class="sxs-lookup"><span data-stu-id="f8e55-113">PARAMETERS</span></span>

### <span data-ttu-id="f8e55-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f8e55-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f8e55-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="f8e55-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-116">-확인</span><span class="sxs-lookup"><span data-stu-id="f8e55-116">-Confirm</span></span>
<span data-ttu-id="f8e55-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e55-118">-DefaultProfile</span></span>
<span data-ttu-id="f8e55-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e55-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f8e55-120">-Name</span></span>
<span data-ttu-id="f8e55-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-121">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8e55-122">-PassThru</span></span>
<span data-ttu-id="f8e55-123">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="f8e55-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-124">This parameter is optional.</span></span> <span data-ttu-id="f8e55-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-125">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e55-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8e55-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8e55-128">-ResourceId</span></span>
<span data-ttu-id="f8e55-129">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8e55-130">-WhatIf</span></span>
<span data-ttu-id="f8e55-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8e55-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e55-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e55-133">CommonParameters</span></span>
<span data-ttu-id="f8e55-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e55-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e55-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e55-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e55-136">입력</span><span class="sxs-lookup"><span data-stu-id="f8e55-136">INPUTS</span></span>

### <span data-ttu-id="f8e55-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f8e55-137">System.String</span></span>

## <span data-ttu-id="f8e55-138">출력</span><span class="sxs-lookup"><span data-stu-id="f8e55-138">OUTPUTS</span></span>

### <span data-ttu-id="f8e55-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="f8e55-139">System.Object</span></span>

## <span data-ttu-id="f8e55-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f8e55-140">NOTES</span></span>

## <span data-ttu-id="f8e55-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8e55-141">RELATED LINKS</span></span>

