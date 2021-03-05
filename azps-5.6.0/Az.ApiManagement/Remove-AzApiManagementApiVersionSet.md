---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 8f505496bc94d7cd0fc4ca69e6a81324a82871d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001952"
---
# <span data-ttu-id="a0269-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a0269-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="a0269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0269-102">SYNOPSIS</span></span>
<span data-ttu-id="a0269-103">특정 Api 버전 집합 제거</span><span class="sxs-lookup"><span data-stu-id="a0269-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="a0269-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0269-104">SYNTAX</span></span>

### <span data-ttu-id="a0269-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="a0269-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0269-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0269-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0269-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0269-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0269-108">설명</span><span class="sxs-lookup"><span data-stu-id="a0269-108">DESCRIPTION</span></span>

<span data-ttu-id="a0269-109">**Remove-AzAzureRmApiManagementApiVersionSet** cmdlet은 기존 API 버전 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="a0269-110">예제</span><span class="sxs-lookup"><span data-stu-id="a0269-110">EXAMPLES</span></span>

### <span data-ttu-id="a0269-111">예제 1: API 버전 집합 제거</span><span class="sxs-lookup"><span data-stu-id="a0269-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="a0269-112">이 명령은 지정된 ApiVersionSetId를 사용하여 API 버전 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="a0269-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a0269-113">PARAMETERS</span></span>

### <span data-ttu-id="a0269-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="a0269-114">-ApiVersionSetId</span></span>
<span data-ttu-id="a0269-115">API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="a0269-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0269-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a0269-117">-Context</span></span>
<span data-ttu-id="a0269-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a0269-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0269-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0269-120">-DefaultProfile</span></span>
<span data-ttu-id="a0269-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0269-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0269-122">-InputObject</span></span>
<span data-ttu-id="a0269-123">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="a0269-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0269-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0269-125">-PassThru</span></span>
<span data-ttu-id="a0269-126">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a0269-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0269-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0269-128">-ResourceId</span></span>
<span data-ttu-id="a0269-129">ApiVersionSet의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="a0269-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0269-131">-확인</span><span class="sxs-lookup"><span data-stu-id="a0269-131">-Confirm</span></span>
<span data-ttu-id="a0269-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0269-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0269-133">-WhatIf</span></span>
<span data-ttu-id="a0269-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0269-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0269-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0269-136">CommonParameters</span></span>
<span data-ttu-id="a0269-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0269-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0269-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0269-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0269-139">입력</span><span class="sxs-lookup"><span data-stu-id="a0269-139">INPUTS</span></span>

### <span data-ttu-id="a0269-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0269-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0269-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a0269-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="a0269-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a0269-142">System.String</span></span>

## <span data-ttu-id="a0269-143">출력</span><span class="sxs-lookup"><span data-stu-id="a0269-143">OUTPUTS</span></span>

### <span data-ttu-id="a0269-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0269-144">System.Boolean</span></span>

## <span data-ttu-id="a0269-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0269-145">NOTES</span></span>

## <span data-ttu-id="a0269-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0269-146">RELATED LINKS</span></span>

[<span data-ttu-id="a0269-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a0269-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="a0269-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a0269-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="a0269-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a0269-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)