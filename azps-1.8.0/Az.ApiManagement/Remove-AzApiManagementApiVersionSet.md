---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869454"
---
# <span data-ttu-id="3fa2f-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3fa2f-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3fa2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fa2f-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa2f-103">특정 Api 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="3fa2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fa2f-104">SYNTAX</span></span>

### <span data-ttu-id="3fa2f-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="3fa2f-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa2f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3fa2f-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa2f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3fa2f-107">DESCRIPTION</span></span>

<span data-ttu-id="3fa2f-108">**AzAzureRmApiManagementApiVersionSet** cmdlet은 기존 API 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="3fa2f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3fa2f-109">EXAMPLES</span></span>

### <span data-ttu-id="3fa2f-110">예제 1: API 버전 집합 제거</span><span class="sxs-lookup"><span data-stu-id="3fa2f-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="3fa2f-111">이 명령은 지정 된 ApiVersionSetId를 사용 하 여 API 버전 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="3fa2f-112">변수</span><span class="sxs-lookup"><span data-stu-id="3fa2f-112">PARAMETERS</span></span>

### <span data-ttu-id="3fa2f-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="3fa2f-113">-ApiVersionSetId</span></span>
<span data-ttu-id="3fa2f-114">API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="3fa2f-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3fa2f-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3fa2f-116">-Context</span></span>
<span data-ttu-id="3fa2f-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3fa2f-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3fa2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa2f-119">-DefaultProfile</span></span>
<span data-ttu-id="3fa2f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa2f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fa2f-121">-InputObject</span></span>
<span data-ttu-id="3fa2f-122">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="3fa2f-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-123">This parameter is required.</span></span>

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

### <span data-ttu-id="3fa2f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fa2f-124">-PassThru</span></span>
<span data-ttu-id="3fa2f-125">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3fa2f-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="3fa2f-127">-확인</span><span class="sxs-lookup"><span data-stu-id="3fa2f-127">-Confirm</span></span>
<span data-ttu-id="3fa2f-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa2f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa2f-129">-WhatIf</span></span>
<span data-ttu-id="3fa2f-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa2f-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa2f-132">CommonParameters</span></span>
<span data-ttu-id="3fa2f-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa2f-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa2f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa2f-135">입력</span><span class="sxs-lookup"><span data-stu-id="3fa2f-135">INPUTS</span></span>

### <span data-ttu-id="3fa2f-136">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3fa2f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3fa2f-137">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3fa2f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="3fa2f-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3fa2f-138">System.String</span></span>

## <span data-ttu-id="3fa2f-139">출력</span><span class="sxs-lookup"><span data-stu-id="3fa2f-139">OUTPUTS</span></span>

### <span data-ttu-id="3fa2f-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3fa2f-140">System.Boolean</span></span>

## <span data-ttu-id="3fa2f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="3fa2f-141">NOTES</span></span>

## <span data-ttu-id="3fa2f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fa2f-142">RELATED LINKS</span></span>

[<span data-ttu-id="3fa2f-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3fa2f-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="3fa2f-144">새로운 AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3fa2f-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="3fa2f-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3fa2f-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)