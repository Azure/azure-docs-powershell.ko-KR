---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: e9981f32422f51910d7e1467f4da0b0c44118f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711713"
---
# <span data-ttu-id="77489-101">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="77489-101">Set-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="77489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77489-102">SYNOPSIS</span></span>
<span data-ttu-id="77489-103">통합 계정 스키마를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-103">Modifies an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77489-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77489-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77489-105">설명은</span><span class="sxs-lookup"><span data-stu-id="77489-105">DESCRIPTION</span></span>
<span data-ttu-id="77489-106">**Set-AzureRmIntegrationAccountSchema** cmdlet은 통합 계정 스키마를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-106">The **Set-AzureRmIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="77489-107">이 cmdlet은 통합 계정 스키마를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="77489-108">통합 계정 이름, 리소스 그룹 이름 및 스키마 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-108">Specify the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="77489-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="77489-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="77489-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="77489-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="77489-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="77489-114">예제의</span><span class="sxs-lookup"><span data-stu-id="77489-114">EXAMPLES</span></span>

### <span data-ttu-id="77489-115">예제 1: 통합 계정 스키마 수정</span><span class="sxs-lookup"><span data-stu-id="77489-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="77489-116">이 명령은 IntegrationAccountSchema43 이라는 통합 계정 스키마를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="77489-117">변수</span><span class="sxs-lookup"><span data-stu-id="77489-117">PARAMETERS</span></span>

### <span data-ttu-id="77489-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="77489-118">-ContentType</span></span>
<span data-ttu-id="77489-119">통합 계정 스키마의 콘텐츠 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="77489-120">이 cmdlet은 응용 프로그램/xml을 맵 콘텐츠 형식으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77489-121">-DefaultProfile</span></span>
<span data-ttu-id="77489-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="77489-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77489-123">-Force</span><span class="sxs-lookup"><span data-stu-id="77489-123">-Force</span></span>
<span data-ttu-id="77489-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="77489-125">-Metadata</span></span>
<span data-ttu-id="77489-126">스키마에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-126">Specifies a metadata object for the schema.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-127">-이름</span><span class="sxs-lookup"><span data-stu-id="77489-127">-Name</span></span>
<span data-ttu-id="77489-128">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-128">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77489-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77489-129">-ResourceGroupName</span></span>
<span data-ttu-id="77489-130">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="77489-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="77489-131">-SchemaDefinition</span></span>
<span data-ttu-id="77489-132">통합 계정 스키마에 대 한 정의 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-132">Specifies a definition object for integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="77489-133">-SchemaFilePath</span></span>
<span data-ttu-id="77489-134">통합 계정 스키마에 대 한 정의의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-134">Specifies the file path of a definition for the integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="77489-135">-SchemaName</span></span>
<span data-ttu-id="77489-136">통합 계정 스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="77489-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="77489-137">-SchemaType</span></span>
<span data-ttu-id="77489-138">통합 계정 스키마의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="77489-139">이 매개 변수는 Xml을 형식으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-140">-확인</span><span class="sxs-lookup"><span data-stu-id="77489-140">-Confirm</span></span>
<span data-ttu-id="77489-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77489-142">-WhatIf</span></span>
<span data-ttu-id="77489-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77489-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77489-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77489-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77489-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77489-145">CommonParameters</span></span>
<span data-ttu-id="77489-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77489-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77489-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77489-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77489-148">입력</span><span class="sxs-lookup"><span data-stu-id="77489-148">INPUTS</span></span>

### <span data-ttu-id="77489-149">않아야</span><span class="sxs-lookup"><span data-stu-id="77489-149">None</span></span>
<span data-ttu-id="77489-150">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77489-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77489-151">출력</span><span class="sxs-lookup"><span data-stu-id="77489-151">OUTPUTS</span></span>

### <span data-ttu-id="77489-152">IntegrationAccountSchema를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="77489-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="77489-153">상속자</span><span class="sxs-lookup"><span data-stu-id="77489-153">NOTES</span></span>

## <span data-ttu-id="77489-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77489-154">RELATED LINKS</span></span>

[<span data-ttu-id="77489-155">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="77489-155">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="77489-156">새로운 AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="77489-156">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="77489-157">제거-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="77489-157">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)


