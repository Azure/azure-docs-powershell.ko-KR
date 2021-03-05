---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 10408574a36018293fd15ef4f258ef4923f21d8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008907"
---
# <span data-ttu-id="96395-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="96395-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="96395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96395-102">SYNOPSIS</span></span>
<span data-ttu-id="96395-103">Logic App 트리거 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96395-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="96395-104">구문</span><span class="sxs-lookup"><span data-stu-id="96395-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96395-105">설명</span><span class="sxs-lookup"><span data-stu-id="96395-105">DESCRIPTION</span></span>
<span data-ttu-id="96395-106">**Get-AzLogicAppTriggerCallbackUrl** cmdlet은 리소스 그룹에서 Logic App 트리거 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96395-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="96395-107">이 cmdlet은 콜백 URL을 나타내는 **WorkflowTriggerCallbackUrl** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="96395-108">리소스 그룹 이름, 논리 앱 이름 및 트리거 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="96395-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="96395-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="96395-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="96395-112">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96395-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="96395-113">예제</span><span class="sxs-lookup"><span data-stu-id="96395-113">EXAMPLES</span></span>

### <span data-ttu-id="96395-114">예제 1: Logic App 트리거 콜백 URL을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="96395-115">이 명령은 Logic App 트리거 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96395-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="96395-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="96395-116">PARAMETERS</span></span>

### <span data-ttu-id="96395-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96395-117">-DefaultProfile</span></span>
<span data-ttu-id="96395-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="96395-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96395-119">-Name</span><span class="sxs-lookup"><span data-stu-id="96395-119">-Name</span></span>
<span data-ttu-id="96395-120">논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96395-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96395-121">-ResourceGroupName</span></span>
<span data-ttu-id="96395-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="96395-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="96395-123">-TriggerName</span></span>
<span data-ttu-id="96395-124">트리거의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="96395-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96395-125">CommonParameters</span></span>
<span data-ttu-id="96395-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96395-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96395-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96395-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96395-128">입력</span><span class="sxs-lookup"><span data-stu-id="96395-128">INPUTS</span></span>

### <span data-ttu-id="96395-129">System.String</span><span class="sxs-lookup"><span data-stu-id="96395-129">System.String</span></span>

## <span data-ttu-id="96395-130">출력</span><span class="sxs-lookup"><span data-stu-id="96395-130">OUTPUTS</span></span>

### <span data-ttu-id="96395-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="96395-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="96395-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96395-132">NOTES</span></span>

## <span data-ttu-id="96395-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96395-133">RELATED LINKS</span></span>

[<span data-ttu-id="96395-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="96395-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


