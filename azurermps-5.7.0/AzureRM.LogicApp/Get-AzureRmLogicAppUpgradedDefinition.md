---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: 532c0883871566326ff6ac97e891ff19755d7656
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532157"
---
# <span data-ttu-id="a0f4b-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="a0f4b-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="a0f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f4b-103">논리 앱에 대 한 업그레이드 된 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0f4b-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0f4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f4b-106">**AzureRmLogicAppUpgradedDefinition** cmdlet은 리소스 그룹의 스키마 버전 및 논리 앱에 대 한 업그레이드 된 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="a0f4b-107">이 cmdlet은 업그레이드 된 논리 앱의 정의를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="a0f4b-108">리소스 그룹 이름, 논리 앱 이름 및 대상 스키마 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-108">Specify the resource group name, logic app name, and target schema version.</span></span>

<span data-ttu-id="a0f4b-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a0f4b-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a0f4b-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a0f4b-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a0f4b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a0f4b-113">EXAMPLES</span></span>

### <span data-ttu-id="a0f4b-114">예제 1: 업그레이드 된 논리 앱 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="a0f4b-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="a0f4b-115">첫 번째 명령은 지정 된 대상 스키마 버전으로 업그레이드 된 논리 앱에 대 한 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="a0f4b-116">명령이 정의를 $UpgradedDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>

<span data-ttu-id="a0f4b-117">두 번째 명령은 $UpgradedDefinition의 내용을 문자열로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="a0f4b-118">변수</span><span class="sxs-lookup"><span data-stu-id="a0f4b-118">PARAMETERS</span></span>

### <span data-ttu-id="a0f4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f4b-119">-DefaultProfile</span></span>
<span data-ttu-id="a0f4b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0f4b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0f4b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a0f4b-121">-Name</span></span>
<span data-ttu-id="a0f4b-122">논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-122">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0f4b-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f4b-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="a0f4b-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="a0f4b-126">정의의 대상 스키마 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f4b-127">CommonParameters</span></span>
<span data-ttu-id="a0f4b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f4b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f4b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f4b-130">입력</span><span class="sxs-lookup"><span data-stu-id="a0f4b-130">INPUTS</span></span>

### <span data-ttu-id="a0f4b-131">않아야</span><span class="sxs-lookup"><span data-stu-id="a0f4b-131">None</span></span>
<span data-ttu-id="a0f4b-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0f4b-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0f4b-133">출력</span><span class="sxs-lookup"><span data-stu-id="a0f4b-133">OUTPUTS</span></span>

### <span data-ttu-id="a0f4b-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a0f4b-134">System.Object</span></span>

## <span data-ttu-id="a0f4b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a0f4b-135">NOTES</span></span>

## <span data-ttu-id="a0f4b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0f4b-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0f4b-137">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f4b-137">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)


