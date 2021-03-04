---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: 7ce86f893cbead5b2c5ac7a57af44eeb7f92f9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958688"
---
# <span data-ttu-id="88eeb-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="88eeb-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="88eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="88eeb-103">통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-103">Creates an integration account map.</span></span>

## <span data-ttu-id="88eeb-104">구문</span><span class="sxs-lookup"><span data-stu-id="88eeb-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88eeb-105">설명</span><span class="sxs-lookup"><span data-stu-id="88eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="88eeb-106">**New-AzIntegrationAccountMap** cmdlet은 통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="88eeb-107">이 cmdlet은 통합 계정 맵을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="88eeb-108">통합 계정 이름, 리소스 그룹 이름, 맵 이름 및 맵 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="88eeb-109">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="88eeb-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="88eeb-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="88eeb-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="88eeb-113">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="88eeb-114">예제</span><span class="sxs-lookup"><span data-stu-id="88eeb-114">EXAMPLES</span></span>

### <span data-ttu-id="88eeb-115">예제 1: 통합 계정 맵 만들기</span><span class="sxs-lookup"><span data-stu-id="88eeb-115">Example 1: Create an integration account map</span></span>
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

<span data-ttu-id="88eeb-116">이 명령은 지정된 리소스 그룹에 통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="88eeb-117">명령은 이전 명령에 의해 $MapContent 변수에 저장된 맵 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="88eeb-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="88eeb-118">Example 2</span></span>

<span data-ttu-id="88eeb-119">통합 계정 맵을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-119">Creates an integration account map.</span></span> <span data-ttu-id="88eeb-120">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="88eeb-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="88eeb-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="88eeb-121">PARAMETERS</span></span>

### <span data-ttu-id="88eeb-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="88eeb-122">-ContentType</span></span>
<span data-ttu-id="88eeb-123">통합 계정 맵에 대한 콘텐츠 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="88eeb-124">이 cmdlet은 애플리케이션/xml을 맵 콘텐츠 유형으로 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="88eeb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88eeb-125">-DefaultProfile</span></span>
<span data-ttu-id="88eeb-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88eeb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88eeb-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="88eeb-127">-MapDefinition</span></span>
<span data-ttu-id="88eeb-128">통합 계정 맵에 대한 정의 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="88eeb-129">이 매개 변수 또는 *MapFilePath* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="88eeb-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="88eeb-130">-MapFilePath</span></span>
<span data-ttu-id="88eeb-131">통합 계정 맵에 대한 정의의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="88eeb-132">이 매개 변수 또는 *MapDefinition 매개 변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="88eeb-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="88eeb-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="88eeb-133">-MapName</span></span>
<span data-ttu-id="88eeb-134">통합 계정 맵의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="88eeb-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="88eeb-135">-MapType</span></span>
<span data-ttu-id="88eeb-136">통합 계정 맵의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="88eeb-137">이 cmdlet은 맵 유형으로 Xslt를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-137">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="88eeb-138">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="88eeb-138">-Metadata</span></span>
<span data-ttu-id="88eeb-139">맵에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="88eeb-140">-Name</span><span class="sxs-lookup"><span data-stu-id="88eeb-140">-Name</span></span>
<span data-ttu-id="88eeb-141">통합 계정에 대한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="88eeb-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88eeb-142">-ResourceGroupName</span></span>
<span data-ttu-id="88eeb-143">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="88eeb-144">-확인</span><span class="sxs-lookup"><span data-stu-id="88eeb-144">-Confirm</span></span>
<span data-ttu-id="88eeb-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88eeb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88eeb-146">-WhatIf</span></span>
<span data-ttu-id="88eeb-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88eeb-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88eeb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88eeb-149">CommonParameters</span></span>
<span data-ttu-id="88eeb-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88eeb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88eeb-151">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88eeb-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88eeb-152">입력</span><span class="sxs-lookup"><span data-stu-id="88eeb-152">INPUTS</span></span>

### <span data-ttu-id="88eeb-153">System.String</span><span class="sxs-lookup"><span data-stu-id="88eeb-153">System.String</span></span>

## <span data-ttu-id="88eeb-154">출력</span><span class="sxs-lookup"><span data-stu-id="88eeb-154">OUTPUTS</span></span>

### <span data-ttu-id="88eeb-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="88eeb-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="88eeb-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88eeb-156">NOTES</span></span>

## <span data-ttu-id="88eeb-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88eeb-157">RELATED LINKS</span></span>

[<span data-ttu-id="88eeb-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="88eeb-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="88eeb-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="88eeb-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="88eeb-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="88eeb-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


