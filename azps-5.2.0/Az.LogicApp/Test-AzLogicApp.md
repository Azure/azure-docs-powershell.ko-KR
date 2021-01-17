---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360466"
---
# <span data-ttu-id="4de46-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4de46-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="4de46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de46-102">SYNOPSIS</span></span>
<span data-ttu-id="4de46-103">논리 앱 정의의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="4de46-104">구문</span><span class="sxs-lookup"><span data-stu-id="4de46-104">SYNTAX</span></span>

### <span data-ttu-id="4de46-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de46-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4de46-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de46-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4de46-107">설명</span><span class="sxs-lookup"><span data-stu-id="4de46-107">DESCRIPTION</span></span>
<span data-ttu-id="4de46-108">**Test-AzLogicApp** cmdlet은 리소스 그룹의 논리 앱 정의의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="4de46-109">논리 앱 이름, 리소스 그룹 이름, 위치, 상태, 통합 계정 ID 또는 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="4de46-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4de46-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4de46-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4de46-113">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4de46-114">예제</span><span class="sxs-lookup"><span data-stu-id="4de46-114">EXAMPLES</span></span>

### <span data-ttu-id="4de46-115">예제 1: 파일 경로를 사용하여 논리 앱 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="4de46-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="4de46-116">이 명령은 지정된 리소스 그룹에서 LogicApp01이라는 논리 앱의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="4de46-117">이 명령은 정의 및 매개 변수 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="4de46-118">예제 2: 개체를 사용하여 논리 앱 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="4de46-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="4de46-119">이 명령은 지정된 리소스 그룹에서 LogicApp01이라는 논리 앱의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="4de46-120">이 명령은 정의 및 매개 변수 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="4de46-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="4de46-121">Example 3</span></span>

<span data-ttu-id="4de46-122">논리 앱 정의의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-122">Validates a logic app definition.</span></span> <span data-ttu-id="4de46-123">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="4de46-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="4de46-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4de46-124">PARAMETERS</span></span>

### <span data-ttu-id="4de46-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de46-125">-DefaultProfile</span></span>
<span data-ttu-id="4de46-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4de46-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4de46-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="4de46-127">-Definition</span></span>
<span data-ttu-id="4de46-128">JSON(JavaScript Object Notation) 형식의 개체 또는 문자열로 논리 앱의 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de46-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="4de46-129">-DefinitionFilePath</span></span>
<span data-ttu-id="4de46-130">JSON 형식의 정의 파일의 경로로 논리 앱의 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de46-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="4de46-131">-IntegrationAccountId</span></span>
<span data-ttu-id="4de46-132">논리 앱에 대한 통합 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="4de46-133">-Location</span><span class="sxs-lookup"><span data-stu-id="4de46-133">-Location</span></span>
<span data-ttu-id="4de46-134">논리 앱의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="4de46-135">Azure 데이터 센터 위치(예: 미국 서부 또는 동남 아시아)를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="4de46-136">논리 앱을 모든 위치에 위치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="4de46-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4de46-137">-Name</span></span>
<span data-ttu-id="4de46-138">논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="4de46-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="4de46-139">-ParameterFilePath</span></span>
<span data-ttu-id="4de46-140">JSON 형식 매개 변수 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="4de46-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4de46-141">-Parameters</span></span>
<span data-ttu-id="4de46-142">논리 앱의 매개 변수 컬렉션 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="4de46-143">해시 테이블, 사전 \<string\> 또는 사전을 \<string, WorkflowParameter\> 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de46-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de46-144">-ResourceGroupName</span></span>
<span data-ttu-id="4de46-145">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4de46-146">-State</span><span class="sxs-lookup"><span data-stu-id="4de46-146">-State</span></span>
<span data-ttu-id="4de46-147">논리 앱의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="4de46-148">이 매개 변수에 허용되는 값은 Enabled 및 Disabled입니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de46-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de46-149">CommonParameters</span></span>
<span data-ttu-id="4de46-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4de46-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de46-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4de46-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de46-152">입력</span><span class="sxs-lookup"><span data-stu-id="4de46-152">INPUTS</span></span>

### <span data-ttu-id="4de46-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4de46-153">System.String</span></span>

## <span data-ttu-id="4de46-154">출력</span><span class="sxs-lookup"><span data-stu-id="4de46-154">OUTPUTS</span></span>

### <span data-ttu-id="4de46-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="4de46-155">System.Void</span></span>

## <span data-ttu-id="4de46-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4de46-156">NOTES</span></span>

## <span data-ttu-id="4de46-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4de46-157">RELATED LINKS</span></span>

[<span data-ttu-id="4de46-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4de46-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="4de46-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4de46-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="4de46-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4de46-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="4de46-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4de46-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="4de46-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4de46-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


