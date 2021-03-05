---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 908c75e2eeb71e864fcdf633511b8eb1c4147401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974816"
---
# <span data-ttu-id="5158f-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5158f-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="5158f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5158f-102">SYNOPSIS</span></span>
<span data-ttu-id="5158f-103">통합 계정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="5158f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5158f-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5158f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5158f-105">DESCRIPTION</span></span>
<span data-ttu-id="5158f-106">**New-AzIntegrationAccountSchema** cmdlet은 통합 계정도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="5158f-107">이 cmdlet은 통합 계정 구성을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="5158f-108">통합 계정 이름, 리소스 그룹 이름, schema 이름 및척도 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="5158f-109">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="5158f-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5158f-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5158f-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5158f-113">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5158f-114">예제</span><span class="sxs-lookup"><span data-stu-id="5158f-114">EXAMPLES</span></span>

### <span data-ttu-id="5158f-115">예제 1: 통합 계정척도 만들기</span><span class="sxs-lookup"><span data-stu-id="5158f-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="5158f-116">이 명령은 지정된 리소스 그룹에 IntegrationAccountSchema1이라는 통합 계정 스마를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="5158f-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5158f-117">PARAMETERS</span></span>

### <span data-ttu-id="5158f-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5158f-118">-ContentType</span></span>
<span data-ttu-id="5158f-119">통합 계정의 콘텐츠 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="5158f-120">이 cmdlet은 애플리케이션/xml을 맵 콘텐츠 유형으로 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="5158f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5158f-121">-DefaultProfile</span></span>
<span data-ttu-id="5158f-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5158f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5158f-123">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="5158f-123">-Metadata</span></span>
<span data-ttu-id="5158f-124">Schema에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="5158f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5158f-125">-Name</span></span>
<span data-ttu-id="5158f-126">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5158f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5158f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5158f-128">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5158f-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="5158f-129">-SchemaDefinition</span></span>
<span data-ttu-id="5158f-130">통합 계정척도에 대한 정의 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="5158f-131">이 매개 변수 또는 *SchemaFilePath* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="5158f-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="5158f-132">-SchemaFilePath</span></span>
<span data-ttu-id="5158f-133">통합 계정척도에 대한 정의의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="5158f-134">이 매개 변수 또는 *SchemaDefinition* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="5158f-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5158f-135">-SchemaName</span></span>
<span data-ttu-id="5158f-136">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="5158f-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="5158f-137">-SchemaType</span></span>
<span data-ttu-id="5158f-138">통합 계정의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="5158f-139">이 매개 변수는 형식으로 Xml을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="5158f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="5158f-140">-Confirm</span></span>
<span data-ttu-id="5158f-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5158f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5158f-142">-WhatIf</span></span>
<span data-ttu-id="5158f-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5158f-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5158f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5158f-145">CommonParameters</span></span>
<span data-ttu-id="5158f-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5158f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5158f-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5158f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5158f-148">입력</span><span class="sxs-lookup"><span data-stu-id="5158f-148">INPUTS</span></span>

### <span data-ttu-id="5158f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="5158f-149">System.String</span></span>

## <span data-ttu-id="5158f-150">출력</span><span class="sxs-lookup"><span data-stu-id="5158f-150">OUTPUTS</span></span>

### <span data-ttu-id="5158f-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5158f-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="5158f-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5158f-152">NOTES</span></span>

## <span data-ttu-id="5158f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5158f-153">RELATED LINKS</span></span>

[<span data-ttu-id="5158f-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5158f-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="5158f-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5158f-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="5158f-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5158f-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


