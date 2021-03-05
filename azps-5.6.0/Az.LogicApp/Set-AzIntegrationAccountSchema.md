---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: cc1c146209758b3ddac9e4b72dcee77e1accf8a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983104"
---
# <span data-ttu-id="201c0-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="201c0-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="201c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201c0-102">SYNOPSIS</span></span>
<span data-ttu-id="201c0-103">통합 계정척도 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="201c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="201c0-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="201c0-105">설명</span><span class="sxs-lookup"><span data-stu-id="201c0-105">DESCRIPTION</span></span>
<span data-ttu-id="201c0-106">**Set-AzIntegrationAccountSchema** cmdlet은 통합 계정 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="201c0-107">이 cmdlet은 통합 계정 구성을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="201c0-108">통합 계정 이름, 리소스 그룹 이름 및 스마마 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="201c0-109">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="201c0-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="201c0-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="201c0-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="201c0-113">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="201c0-114">예제</span><span class="sxs-lookup"><span data-stu-id="201c0-114">EXAMPLES</span></span>

### <span data-ttu-id="201c0-115">예제 1: 통합 계정척도 수정</span><span class="sxs-lookup"><span data-stu-id="201c0-115">Example 1: Modify an integration account schema</span></span>
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

<span data-ttu-id="201c0-116">이 명령은 IntegrationAccountSchema43이라는 통합 계정스마를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="201c0-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="201c0-117">PARAMETERS</span></span>

### <span data-ttu-id="201c0-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="201c0-118">-ContentType</span></span>
<span data-ttu-id="201c0-119">통합 계정의 콘텐츠 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="201c0-120">이 cmdlet은 애플리케이션/xml을 맵 콘텐츠 유형으로 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="201c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201c0-121">-DefaultProfile</span></span>
<span data-ttu-id="201c0-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="201c0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="201c0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="201c0-123">-Force</span></span>
<span data-ttu-id="201c0-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="201c0-125">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="201c0-125">-Metadata</span></span>
<span data-ttu-id="201c0-126">Schema에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="201c0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="201c0-127">-Name</span></span>
<span data-ttu-id="201c0-128">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="201c0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201c0-129">-ResourceGroupName</span></span>
<span data-ttu-id="201c0-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="201c0-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="201c0-131">-SchemaDefinition</span></span>
<span data-ttu-id="201c0-132">통합 계정척도에 대한 정의 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="201c0-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="201c0-133">-SchemaFilePath</span></span>
<span data-ttu-id="201c0-134">통합 계정척도에 대한 정의의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="201c0-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="201c0-135">-SchemaName</span></span>
<span data-ttu-id="201c0-136">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="201c0-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="201c0-137">-SchemaType</span></span>
<span data-ttu-id="201c0-138">통합 계정의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="201c0-139">이 매개 변수는 형식으로 Xml을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="201c0-140">-확인</span><span class="sxs-lookup"><span data-stu-id="201c0-140">-Confirm</span></span>
<span data-ttu-id="201c0-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="201c0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="201c0-142">-WhatIf</span></span>
<span data-ttu-id="201c0-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="201c0-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="201c0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201c0-145">CommonParameters</span></span>
<span data-ttu-id="201c0-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="201c0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201c0-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="201c0-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201c0-148">입력</span><span class="sxs-lookup"><span data-stu-id="201c0-148">INPUTS</span></span>

### <span data-ttu-id="201c0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="201c0-149">System.String</span></span>

## <span data-ttu-id="201c0-150">출력</span><span class="sxs-lookup"><span data-stu-id="201c0-150">OUTPUTS</span></span>

### <span data-ttu-id="201c0-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="201c0-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="201c0-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="201c0-152">NOTES</span></span>

## <span data-ttu-id="201c0-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="201c0-153">RELATED LINKS</span></span>

[<span data-ttu-id="201c0-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="201c0-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="201c0-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="201c0-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="201c0-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="201c0-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


