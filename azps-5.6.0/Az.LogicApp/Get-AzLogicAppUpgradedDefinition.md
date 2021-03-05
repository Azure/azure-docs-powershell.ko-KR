---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 1be662b88b487fbf79092c30f8bd7277adc9e3cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008875"
---
# <span data-ttu-id="fe177-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="fe177-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="fe177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe177-102">SYNOPSIS</span></span>
<span data-ttu-id="fe177-103">논리 앱에 대한 업그레이드된 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="fe177-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe177-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe177-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe177-105">DESCRIPTION</span></span>
<span data-ttu-id="fe177-106">**Get-AzLogicAppUpgradedDefinition** cmdlet은 리소스 그룹에서 schema 버전 및 논리 앱에 대한 업그레이드된 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="fe177-107">이 cmdlet은 업그레이드된 논리 앱의 정의를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="fe177-108">리소스 그룹 이름, 논리 앱 이름 및 대상 schema 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="fe177-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fe177-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fe177-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fe177-112">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fe177-113">예제</span><span class="sxs-lookup"><span data-stu-id="fe177-113">EXAMPLES</span></span>

### <span data-ttu-id="fe177-114">예제 1: 논리 앱 업그레이드 정의를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="fe177-115">첫 번째 명령은 지정된 대상척도 버전으로 업그레이드된 논리 앱에 대한 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="fe177-116">명령은 정의를 $UpgradedDefinition 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="fe177-117">두 번째 명령은 문자열로 $UpgradedDefinition 내용을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="fe177-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe177-118">PARAMETERS</span></span>

### <span data-ttu-id="fe177-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe177-119">-DefaultProfile</span></span>
<span data-ttu-id="fe177-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fe177-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe177-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe177-121">-Name</span></span>
<span data-ttu-id="fe177-122">논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="fe177-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe177-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe177-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fe177-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="fe177-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="fe177-126">정의의 대상 schema 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe177-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe177-127">CommonParameters</span></span>
<span data-ttu-id="fe177-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe177-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe177-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe177-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe177-130">입력</span><span class="sxs-lookup"><span data-stu-id="fe177-130">INPUTS</span></span>

### <span data-ttu-id="fe177-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fe177-131">System.String</span></span>

## <span data-ttu-id="fe177-132">출력</span><span class="sxs-lookup"><span data-stu-id="fe177-132">OUTPUTS</span></span>

### <span data-ttu-id="fe177-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="fe177-133">System.Object</span></span>

## <span data-ttu-id="fe177-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe177-134">NOTES</span></span>

## <span data-ttu-id="fe177-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe177-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe177-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe177-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


