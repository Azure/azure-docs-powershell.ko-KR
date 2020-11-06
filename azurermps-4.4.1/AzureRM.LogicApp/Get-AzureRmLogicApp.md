---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 891f7fcd50281f5dab9b8d4eaf9f1bd842fbc85e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527491"
---
# <span data-ttu-id="65458-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="65458-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="65458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65458-102">SYNOPSIS</span></span>
<span data-ttu-id="65458-103">리소스 그룹에서 논리 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65458-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65458-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65458-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65458-105">DESCRIPTION</span></span>
<span data-ttu-id="65458-106">**Get-AzureRmLogicApp** cmdlet은 논리 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65458-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="65458-107">이 cmdlet은 **워크플로** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="65458-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="65458-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="65458-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="65458-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="65458-112">예제의</span><span class="sxs-lookup"><span data-stu-id="65458-112">EXAMPLES</span></span>

### <span data-ttu-id="65458-113">예제 1: 리소스 그룹에서 논리 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="65458-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="65458-114">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 논리 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65458-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="65458-115">변수</span><span class="sxs-lookup"><span data-stu-id="65458-115">PARAMETERS</span></span>

### <span data-ttu-id="65458-116">-이름</span><span class="sxs-lookup"><span data-stu-id="65458-116">-Name</span></span>
<span data-ttu-id="65458-117">이 cmdlet이 가져오는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-117">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65458-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65458-118">-ResourceGroupName</span></span>
<span data-ttu-id="65458-119">이 cmdlet이 논리 앱을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-119">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="65458-120">-버전</span><span class="sxs-lookup"><span data-stu-id="65458-120">-Version</span></span>
<span data-ttu-id="65458-121">논리 앱의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-121">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65458-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65458-122">-DefaultProfile</span></span>
<span data-ttu-id="65458-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65458-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65458-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65458-124">CommonParameters</span></span>
<span data-ttu-id="65458-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65458-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65458-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65458-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65458-127">입력</span><span class="sxs-lookup"><span data-stu-id="65458-127">INPUTS</span></span>

## <span data-ttu-id="65458-128">출력</span><span class="sxs-lookup"><span data-stu-id="65458-128">OUTPUTS</span></span>

### <span data-ttu-id="65458-129">Microsoft. Azure. 관리 워크플로</span><span class="sxs-lookup"><span data-stu-id="65458-129">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="65458-130">상속자</span><span class="sxs-lookup"><span data-stu-id="65458-130">NOTES</span></span>

## <span data-ttu-id="65458-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65458-131">RELATED LINKS</span></span>

[<span data-ttu-id="65458-132">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="65458-132">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="65458-133">제거-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="65458-133">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="65458-134">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="65458-134">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="65458-135">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="65458-135">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


