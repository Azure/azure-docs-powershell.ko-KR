---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 98232807cc5f7624242cd44c7d27579ef0f92d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958699"
---
# <span data-ttu-id="ada17-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ada17-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="ada17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada17-102">SYNOPSIS</span></span>
<span data-ttu-id="ada17-103">리소스 그룹에서 논리 앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="ada17-104">구문</span><span class="sxs-lookup"><span data-stu-id="ada17-104">SYNTAX</span></span>

### <span data-ttu-id="ada17-105">ListWorkflows(기본값)</span><span class="sxs-lookup"><span data-stu-id="ada17-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ada17-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="ada17-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada17-107">설명</span><span class="sxs-lookup"><span data-stu-id="ada17-107">DESCRIPTION</span></span>
<span data-ttu-id="ada17-108">**Get-AzLogicApp** cmdlet은 논리 앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="ada17-109">이 cmdlet은 **워크플로** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="ada17-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ada17-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ada17-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ada17-113">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ada17-114">예제</span><span class="sxs-lookup"><span data-stu-id="ada17-114">EXAMPLES</span></span>

### <span data-ttu-id="ada17-115">예제 1: 리소스 그룹에서 논리 앱 다운로드</span><span class="sxs-lookup"><span data-stu-id="ada17-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="ada17-116">이 명령은 ResourceGroup11이라는 리소스 그룹에서 논리 앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ada17-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ada17-117">PARAMETERS</span></span>

### <span data-ttu-id="ada17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada17-118">-DefaultProfile</span></span>
<span data-ttu-id="ada17-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ada17-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ada17-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ada17-120">-Name</span></span>
<span data-ttu-id="ada17-121">이 cmdlet이 얻을 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada17-122">-ResourceGroupName</span></span>
<span data-ttu-id="ada17-123">이 cmdlet에서 논리 앱을 얻을 수 있는 리소스 그룹에 대한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada17-124">-Version</span><span class="sxs-lookup"><span data-stu-id="ada17-124">-Version</span></span>
<span data-ttu-id="ada17-125">논리 앱의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada17-126">CommonParameters</span></span>
<span data-ttu-id="ada17-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ada17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada17-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ada17-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada17-129">입력</span><span class="sxs-lookup"><span data-stu-id="ada17-129">INPUTS</span></span>

### <span data-ttu-id="ada17-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ada17-130">System.String</span></span>

## <span data-ttu-id="ada17-131">출력</span><span class="sxs-lookup"><span data-stu-id="ada17-131">OUTPUTS</span></span>

### <span data-ttu-id="ada17-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="ada17-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="ada17-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="ada17-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="ada17-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ada17-134">NOTES</span></span>

## <span data-ttu-id="ada17-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ada17-135">RELATED LINKS</span></span>

[<span data-ttu-id="ada17-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ada17-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="ada17-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ada17-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="ada17-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ada17-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="ada17-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ada17-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


