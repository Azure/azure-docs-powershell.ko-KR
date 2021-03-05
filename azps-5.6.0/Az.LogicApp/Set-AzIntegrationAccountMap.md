---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: f963a89e6220e8154c2ba958adca318036c53474
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972736"
---
# <span data-ttu-id="4ce37-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4ce37-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="4ce37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce37-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce37-103">통합 계정 맵을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="4ce37-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ce37-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce37-105">설명</span><span class="sxs-lookup"><span data-stu-id="4ce37-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce37-106">**Set-AzIntegrationAccountMap** cmdlet은 통합 계정 맵을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="4ce37-107">이 cmdlet은 통합 계정 맵을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="4ce37-108">통합 계정 이름, 리소스 그룹 이름 및 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="4ce37-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4ce37-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4ce37-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4ce37-112">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4ce37-113">예제</span><span class="sxs-lookup"><span data-stu-id="4ce37-113">EXAMPLES</span></span>

### <span data-ttu-id="4ce37-114">예제 1: 통합 계정 맵 수정</span><span class="sxs-lookup"><span data-stu-id="4ce37-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="4ce37-115">이 명령은 지정된 리소스 그룹의 통합 계정 맵을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="4ce37-116">명령은 이전 명령에 의해 $MapContent 변수에 저장된 맵 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="4ce37-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="4ce37-117">Example 2</span></span>

<span data-ttu-id="4ce37-118">통합 계정 맵을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-118">Modifies an integration account map.</span></span> <span data-ttu-id="4ce37-119">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="4ce37-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="4ce37-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ce37-120">PARAMETERS</span></span>

### <span data-ttu-id="4ce37-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="4ce37-121">-ContentType</span></span>
<span data-ttu-id="4ce37-122">통합 계정 맵에 대한 콘텐츠 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="4ce37-123">이 cmdlet은 애플리케이션/xml을 맵 콘텐츠 유형으로 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="4ce37-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce37-124">-DefaultProfile</span></span>
<span data-ttu-id="4ce37-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ce37-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ce37-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4ce37-126">-Force</span></span>
<span data-ttu-id="4ce37-127">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ce37-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="4ce37-128">-MapDefinition</span></span>
<span data-ttu-id="4ce37-129">통합 계정 맵에 대한 정의 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="4ce37-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="4ce37-130">-MapFilePath</span></span>
<span data-ttu-id="4ce37-131">통합 계정 맵에 대한 정의의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="4ce37-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="4ce37-132">-MapName</span></span>
<span data-ttu-id="4ce37-133">통합 계정 맵의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="4ce37-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="4ce37-134">-MapType</span></span>
<span data-ttu-id="4ce37-135">통합 계정 맵의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="4ce37-136">이 cmdlet은 맵 유형으로 Xslt를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="4ce37-137">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="4ce37-137">-Metadata</span></span>
<span data-ttu-id="4ce37-138">맵에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="4ce37-139">-Name</span><span class="sxs-lookup"><span data-stu-id="4ce37-139">-Name</span></span>
<span data-ttu-id="4ce37-140">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="4ce37-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce37-141">-ResourceGroupName</span></span>
<span data-ttu-id="4ce37-142">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4ce37-143">-확인</span><span class="sxs-lookup"><span data-stu-id="4ce37-143">-Confirm</span></span>
<span data-ttu-id="4ce37-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce37-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce37-145">-WhatIf</span></span>
<span data-ttu-id="4ce37-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce37-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce37-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce37-148">CommonParameters</span></span>
<span data-ttu-id="4ce37-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce37-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce37-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ce37-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce37-151">입력</span><span class="sxs-lookup"><span data-stu-id="4ce37-151">INPUTS</span></span>

### <span data-ttu-id="4ce37-152">System.String</span><span class="sxs-lookup"><span data-stu-id="4ce37-152">System.String</span></span>

## <span data-ttu-id="4ce37-153">출력</span><span class="sxs-lookup"><span data-stu-id="4ce37-153">OUTPUTS</span></span>

### <span data-ttu-id="4ce37-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4ce37-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="4ce37-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ce37-155">NOTES</span></span>

## <span data-ttu-id="4ce37-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ce37-156">RELATED LINKS</span></span>

[<span data-ttu-id="4ce37-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4ce37-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="4ce37-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4ce37-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="4ce37-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4ce37-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


