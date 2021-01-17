---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368355"
---
# <span data-ttu-id="df29f-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="df29f-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="df29f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df29f-102">SYNOPSIS</span></span>
<span data-ttu-id="df29f-103">통합 계정 스마마를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="df29f-104">구문</span><span class="sxs-lookup"><span data-stu-id="df29f-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df29f-105">설명</span><span class="sxs-lookup"><span data-stu-id="df29f-105">DESCRIPTION</span></span>
<span data-ttu-id="df29f-106">**Set-AzIntegrationAccountSchema** cmdlet은 통합 계정 스마마를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="df29f-107">이 cmdlet은 통합 계정 키마를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="df29f-108">통합 계정 이름, 리소스 그룹 이름 및 스마마 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="df29f-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="df29f-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="df29f-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="df29f-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="df29f-113">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="df29f-114">예제</span><span class="sxs-lookup"><span data-stu-id="df29f-114">EXAMPLES</span></span>

### <span data-ttu-id="df29f-115">예제 1: 통합 계정 schema 수정</span><span class="sxs-lookup"><span data-stu-id="df29f-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="df29f-116">이 명령은 IntegrationAccountSchema43이라는 통합 계정 스마마를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="df29f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df29f-117">PARAMETERS</span></span>

### <span data-ttu-id="df29f-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="df29f-118">-ContentType</span></span>
<span data-ttu-id="df29f-119">통합 계정의 콘텐츠 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="df29f-120">이 cmdlet은 맵 콘텐츠 유형으로 application/xml을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="df29f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df29f-121">-DefaultProfile</span></span>
<span data-ttu-id="df29f-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="df29f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df29f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="df29f-123">-Force</span></span>
<span data-ttu-id="df29f-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df29f-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="df29f-125">-Metadata</span></span>
<span data-ttu-id="df29f-126">스마마에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="df29f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="df29f-127">-Name</span></span>
<span data-ttu-id="df29f-128">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="df29f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df29f-129">-ResourceGroupName</span></span>
<span data-ttu-id="df29f-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="df29f-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="df29f-131">-SchemaDefinition</span></span>
<span data-ttu-id="df29f-132">통합 계정 스마마에 대한 정의 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="df29f-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="df29f-133">-SchemaFilePath</span></span>
<span data-ttu-id="df29f-134">통합 계정 스마마에 대한 정의의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="df29f-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="df29f-135">-SchemaName</span></span>
<span data-ttu-id="df29f-136">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="df29f-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="df29f-137">-SchemaType</span></span>
<span data-ttu-id="df29f-138">통합 계정의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="df29f-139">이 매개 변수는 Xml을 유형으로 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df29f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df29f-140">-Confirm</span></span>
<span data-ttu-id="df29f-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df29f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df29f-142">-WhatIf</span></span>
<span data-ttu-id="df29f-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df29f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df29f-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df29f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df29f-145">CommonParameters</span></span>
<span data-ttu-id="df29f-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df29f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df29f-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df29f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df29f-148">입력</span><span class="sxs-lookup"><span data-stu-id="df29f-148">INPUTS</span></span>

### <span data-ttu-id="df29f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="df29f-149">System.String</span></span>

## <span data-ttu-id="df29f-150">출력</span><span class="sxs-lookup"><span data-stu-id="df29f-150">OUTPUTS</span></span>

### <span data-ttu-id="df29f-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="df29f-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="df29f-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df29f-152">NOTES</span></span>

## <span data-ttu-id="df29f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df29f-153">RELATED LINKS</span></span>

[<span data-ttu-id="df29f-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="df29f-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="df29f-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="df29f-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="df29f-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="df29f-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


