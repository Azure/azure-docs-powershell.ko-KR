---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190321"
---
# <span data-ttu-id="87372-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="87372-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="87372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87372-102">SYNOPSIS</span></span>
<span data-ttu-id="87372-103">논리 앱 트리거 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87372-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="87372-104">구문</span><span class="sxs-lookup"><span data-stu-id="87372-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87372-105">설명</span><span class="sxs-lookup"><span data-stu-id="87372-105">DESCRIPTION</span></span>
<span data-ttu-id="87372-106">**Get-AzLogicAppTriggerCallbackUrl** cmdlet은 리소스 그룹에서 논리 앱 트리거 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87372-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="87372-107">이 cmdlet은 콜백 URL을 나타내는 **WorkflowTriggerCallbackUrl** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="87372-108">리소스 그룹 이름, 논리 앱 이름 및 트리거 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="87372-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="87372-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="87372-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="87372-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="87372-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="87372-113">예제</span><span class="sxs-lookup"><span data-stu-id="87372-113">EXAMPLES</span></span>

### <span data-ttu-id="87372-114">예제 1: 논리 앱 트리거 콜백 URL을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="87372-115">이 명령은 논리 앱 트리거 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87372-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="87372-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87372-116">PARAMETERS</span></span>

### <span data-ttu-id="87372-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87372-117">-DefaultProfile</span></span>
<span data-ttu-id="87372-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="87372-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87372-119">-Name</span><span class="sxs-lookup"><span data-stu-id="87372-119">-Name</span></span>
<span data-ttu-id="87372-120">논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="87372-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87372-121">-ResourceGroupName</span></span>
<span data-ttu-id="87372-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="87372-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="87372-123">-TriggerName</span></span>
<span data-ttu-id="87372-124">트리거의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="87372-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87372-125">CommonParameters</span></span>
<span data-ttu-id="87372-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87372-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87372-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87372-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87372-128">입력</span><span class="sxs-lookup"><span data-stu-id="87372-128">INPUTS</span></span>

### <span data-ttu-id="87372-129">System.String</span><span class="sxs-lookup"><span data-stu-id="87372-129">System.String</span></span>

## <span data-ttu-id="87372-130">출력</span><span class="sxs-lookup"><span data-stu-id="87372-130">OUTPUTS</span></span>

### <span data-ttu-id="87372-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="87372-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="87372-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87372-132">NOTES</span></span>

## <span data-ttu-id="87372-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87372-133">RELATED LINKS</span></span>

[<span data-ttu-id="87372-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="87372-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


