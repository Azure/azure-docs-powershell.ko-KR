---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: a7803d95c2991dd829053a6d508432931701a220
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203716"
---
# <span data-ttu-id="b313d-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b313d-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="b313d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b313d-102">SYNOPSIS</span></span>
<span data-ttu-id="b313d-103">통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-103">Creates an integration account map.</span></span>

## <span data-ttu-id="b313d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b313d-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b313d-105">설명</span><span class="sxs-lookup"><span data-stu-id="b313d-105">DESCRIPTION</span></span>
<span data-ttu-id="b313d-106">**New-AzIntegrationAccountMap** cmdlet은 통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="b313d-107">이 cmdlet은 통합 계정 맵을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="b313d-108">통합 계정 이름, 리소스 그룹 이름, 맵 이름 및 맵 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="b313d-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b313d-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b313d-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b313d-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b313d-113">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b313d-114">예제</span><span class="sxs-lookup"><span data-stu-id="b313d-114">EXAMPLES</span></span>

### <span data-ttu-id="b313d-115">예제 1: 통합 계정 맵 만들기</span><span class="sxs-lookup"><span data-stu-id="b313d-115">Example 1: Create an integration account map</span></span>
```powershell
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="b313d-116">이 명령은 지정된 리소스 그룹에 통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="b313d-117">이 명령은 이전 명령으로 $MapContent 변수에 저장된 맵 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="b313d-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="b313d-118">Example 2</span></span>

<span data-ttu-id="b313d-119">통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-119">Creates an integration account map.</span></span> <span data-ttu-id="b313d-120">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="b313d-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="b313d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b313d-121">PARAMETERS</span></span>

### <span data-ttu-id="b313d-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b313d-122">-ContentType</span></span>
<span data-ttu-id="b313d-123">통합 계정 맵에 대한 콘텐츠 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="b313d-124">이 cmdlet은 맵 콘텐츠 유형으로 application/xml을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="b313d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b313d-125">-DefaultProfile</span></span>
<span data-ttu-id="b313d-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b313d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b313d-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="b313d-127">-MapDefinition</span></span>
<span data-ttu-id="b313d-128">통합 계정 맵에 대한 정의 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="b313d-129">이 매개 변수 또는 *MapFilePath* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="b313d-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="b313d-130">-MapFilePath</span></span>
<span data-ttu-id="b313d-131">통합 계정 맵에 대한 정의의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="b313d-132">이 매개 변수 또는 *MapDefinition* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="b313d-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="b313d-133">-MapName</span></span>
<span data-ttu-id="b313d-134">통합 계정 맵의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="b313d-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="b313d-135">-MapType</span></span>
<span data-ttu-id="b313d-136">통합 계정 맵의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="b313d-137">이 cmdlet은 맵 유형으로 Xslt를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-137">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313d-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b313d-138">-Metadata</span></span>
<span data-ttu-id="b313d-139">맵에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="b313d-140">-Name</span><span class="sxs-lookup"><span data-stu-id="b313d-140">-Name</span></span>
<span data-ttu-id="b313d-141">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-141">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b313d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b313d-142">-ResourceGroupName</span></span>
<span data-ttu-id="b313d-143">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b313d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b313d-144">-Confirm</span></span>
<span data-ttu-id="b313d-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b313d-146">-WhatIf</span></span>
<span data-ttu-id="b313d-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b313d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b313d-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b313d-149">CommonParameters</span></span>
<span data-ttu-id="b313d-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b313d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b313d-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b313d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b313d-152">입력</span><span class="sxs-lookup"><span data-stu-id="b313d-152">INPUTS</span></span>

### <span data-ttu-id="b313d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b313d-153">System.String</span></span>

## <span data-ttu-id="b313d-154">출력</span><span class="sxs-lookup"><span data-stu-id="b313d-154">OUTPUTS</span></span>

### <span data-ttu-id="b313d-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b313d-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b313d-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b313d-156">NOTES</span></span>

## <span data-ttu-id="b313d-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b313d-157">RELATED LINKS</span></span>

[<span data-ttu-id="b313d-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b313d-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="b313d-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b313d-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="b313d-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b313d-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


