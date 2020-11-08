---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042161"
---
# <span data-ttu-id="5b98a-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5b98a-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="5b98a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b98a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b98a-103">특정 Api 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="5b98a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b98a-104">SYNTAX</span></span>

### <span data-ttu-id="5b98a-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="5b98a-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b98a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b98a-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b98a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b98a-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b98a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5b98a-108">DESCRIPTION</span></span>

<span data-ttu-id="5b98a-109">**AzAzureRmApiManagementApiVersionSet** cmdlet은 기존 API 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="5b98a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5b98a-110">EXAMPLES</span></span>

### <span data-ttu-id="5b98a-111">예제 1: API 버전 집합 제거</span><span class="sxs-lookup"><span data-stu-id="5b98a-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="5b98a-112">이 명령은 지정 된 ApiVersionSetId를 사용 하 여 API 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="5b98a-113">변수</span><span class="sxs-lookup"><span data-stu-id="5b98a-113">PARAMETERS</span></span>

### <span data-ttu-id="5b98a-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="5b98a-114">-ApiVersionSetId</span></span>
<span data-ttu-id="5b98a-115">API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="5b98a-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-116">This parameter is required.</span></span>

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

### <span data-ttu-id="5b98a-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5b98a-117">-Context</span></span>
<span data-ttu-id="5b98a-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5b98a-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="5b98a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b98a-120">-DefaultProfile</span></span>
<span data-ttu-id="5b98a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b98a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b98a-122">-InputObject</span></span>
<span data-ttu-id="5b98a-123">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="5b98a-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="5b98a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b98a-125">-PassThru</span></span>
<span data-ttu-id="5b98a-126">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="5b98a-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="5b98a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b98a-128">-ResourceId</span></span>
<span data-ttu-id="5b98a-129">ApiVersionSet의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="5b98a-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-130">This parameter is required.</span></span>

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

### <span data-ttu-id="5b98a-131">-확인</span><span class="sxs-lookup"><span data-stu-id="5b98a-131">-Confirm</span></span>
<span data-ttu-id="5b98a-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b98a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b98a-133">-WhatIf</span></span>
<span data-ttu-id="5b98a-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b98a-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b98a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b98a-136">CommonParameters</span></span>
<span data-ttu-id="5b98a-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b98a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b98a-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b98a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b98a-139">입력</span><span class="sxs-lookup"><span data-stu-id="5b98a-139">INPUTS</span></span>

### <span data-ttu-id="5b98a-140">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5b98a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5b98a-141">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5b98a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="5b98a-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b98a-142">System.String</span></span>

## <span data-ttu-id="5b98a-143">출력</span><span class="sxs-lookup"><span data-stu-id="5b98a-143">OUTPUTS</span></span>

### <span data-ttu-id="5b98a-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5b98a-144">System.Boolean</span></span>

## <span data-ttu-id="5b98a-145">상속자</span><span class="sxs-lookup"><span data-stu-id="5b98a-145">NOTES</span></span>

## <span data-ttu-id="5b98a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b98a-146">RELATED LINKS</span></span>

[<span data-ttu-id="5b98a-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5b98a-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="5b98a-148">새로운 AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5b98a-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="5b98a-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5b98a-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)